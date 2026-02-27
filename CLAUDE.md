# Waterloo Rocketry 2025 Software Issues — Claude Instructions

## Repository Context

This is an **issue-tracking repo only** — it contains no application code and **PRs should never be opened here** (except for reports). All code PRs live in the linked implementation repos listed below.

### Issue Hierarchy

Issues follow a 4-level hierarchy:
- **Project** (label: `project`) — high-level initiatives spanning months
- **Epic** (label: `epic`) — goals/features, 1–2 months
- **Story** (label: `story`) — individual features, 1–2 weeks
- **Task** (label: `task`) — individual tasks, a few hours

### Label Conventions

- Each project issue gets a `project-<name>` label (e.g., `project-1`, `project-daqms`)
- Child issues (epics/stories/tasks) carry the parent's `project-N` label to link them
- Additional labels: `bug`, `feature`, `good first issue`, `help wanted`, `urgent`, `blocked`

### Linked Implementation Repos

Code PRs for issues tracked here live in these `waterloo-rocketry` org repos:
- `omnibus` — core infrastructure
- `omnibus-DAQms` — DAQ ops frontend
- `omnibus-avionics-testing-app` — avionics testing app
- `omnibus-ts` — TypeScript library
- `parsley` — log parser
- `website-react` — team website

---

## Skills

### /status-report

Generate a comprehensive project status report for the software design cycle.

**Trigger:** User runs `/status-report`

#### Step 1: Fetch all issues

```bash
gh issue list --repo waterloo-rocketry/2025-software-issues --state all --limit 200 --json number,title,author,assignees,labels,state,createdAt,updatedAt,url,body > /tmp/all_issues.json
```

#### Step 2: Parse issues into a structured summary

```bash
cat /tmp/all_issues.json | python3 -c "
import json, sys
data = json.load(sys.stdin)
for i in data:
    assignees = ','.join([a['login'] for a in i['assignees']]) or 'unassigned'
    labels = ','.join([l['name'] for l in i['labels']])
    print(f\"{i['number']}|{i['state']}|{assignees}|{labels}|{i['updatedAt'][:10]}|{i['title']}\")
"
```

#### Step 3: Identify projects, epics, and relationships

Extract project issues and their bodies for context:

```bash
cat /tmp/all_issues.json | python3 -c "
import json, sys
data = json.load(sys.stdin)
projects = [i for i in data if any(l['name'] == 'project' for l in i['labels'])]
for p in projects:
    print(f'=== Issue #{p[\"number\"]}: {p[\"title\"]} ===')
    print(f'State: {p[\"state\"]}')
    print(f'Body (first 1500 chars):')
    print((p['body'] or '')[:1500])
    print()
"
```

Extract epic issues:

```bash
cat /tmp/all_issues.json | python3 -c "
import json, sys
data = json.load(sys.stdin)
epics = [i for i in data if any(l['name'] == 'epic' for l in i['labels'])]
for e in epics:
    assignees = ','.join([a['login'] for a in e['assignees']]) or 'unassigned'
    print(f'=== Epic #{e[\"number\"]}: {e[\"title\"]} | Assigned: {assignees} | State: {e[\"state\"]} ===')
    print((e['body'] or '')[:800])
    print()
"
```

List all closed issues:

```bash
cat /tmp/all_issues.json | python3 -c "
import json, sys
data = json.load(sys.stdin)
closed = [i for i in data if i['state'] == 'CLOSED']
print('CLOSED ISSUES:')
for i in closed:
    labels = ','.join([l['name'] for l in i['labels']])
    assignees = ','.join([a['login'] for a in i['assignees']]) or 'unassigned'
    print(f'  #{i[\"number\"]} {i[\"title\"]} | {assignees} | {labels} | closed ~{i[\"updatedAt\"][:10]}')
"
```

#### Step 4: Fetch linked PRs across the org

Search for PRs that reference this issues repo org-wide:

```bash
gh search prs "2025-software-issues" --owner waterloo-rocketry --limit 50 --json number,title,author,state,repository,url,updatedAt
```

Fetch PRs from each linked implementation repo:

```bash
gh pr list --repo waterloo-rocketry/omnibus --state all --limit 50 --json number,title,author,state,updatedAt,url
gh pr list --repo waterloo-rocketry/omnibus-DAQms --state all --limit 50 --json number,title,author,state,updatedAt,url
gh pr list --repo waterloo-rocketry/omnibus-avionics-testing-app --state all --limit 50 --json number,title,author,state,updatedAt,url
gh pr list --repo waterloo-rocketry/omnibus-ts --state all --limit 50 --json number,title,author,state,updatedAt,url
gh pr list --repo waterloo-rocketry/parsley --state all --limit 50 --json number,title,author,state,updatedAt,url
gh pr list --repo waterloo-rocketry/website-react --state all --limit 50 --json number,title,author,state,updatedAt,url
```

#### Step 5: Fetch comment counts for open assigned issues

Get comment counts to gauge activity on open issues. Build the issue number list dynamically from the parsed data, then loop:

```bash
# Extract open assigned issue numbers from /tmp/all_issues.json, then fetch comment counts
ISSUE_NUMS=$(cat /tmp/all_issues.json | python3 -c "
import json, sys
data = json.load(sys.stdin)
nums = [str(i['number']) for i in data if i['state'] == 'OPEN' and i['assignees']]
print(' '.join(nums))
")
for issue_num in $ISSUE_NUMS; do
  count=$(gh api repos/waterloo-rocketry/2025-software-issues/issues/$issue_num/comments --jq 'length' 2>/dev/null || echo "0")
  echo "$issue_num|$count"
done
```

#### Step 6: Optionally fetch issue timelines for key issues

For issues that need deeper activity analysis, fetch timeline events:

```bash
# Use this for issues where you need to check cross-reference events
gh api repos/waterloo-rocketry/2025-software-issues/issues/{NUMBER}/timeline --jq '.[] | select(.event != null) | "\(.event) by \(.actor.login // "unknown") at \(.created_at // .updated_at // "unknown")"' 2>/dev/null | tail -5
```

#### Step 7: Analyze and produce the report

Using all the data gathered above, produce a markdown report with **exactly 3 sections**:

##### Section 1: Who's Working on What Right Now

- Group by contributor (GitHub username)
- For each contributor, list:
  - Active PRs (open PRs across linked repos) with links and dates
  - Assigned open issues with links
  - Recently completed/closed issues
  - Epic/project leadership roles (if they own an epic or project issue)
- Format each contributor as `### GitHubUsername`

##### Section 2: Stale Tasks

- **Definition of stale:** An issue is stale if it is **assigned**, **open**, and its `updatedAt` is **more than 30 days ago**, with **no recent linked PR activity** in linked repos.
- Present as a markdown table with columns: `| Issue | Title | Assignee(s) | Last Updated | Notes |`
- In the Notes column, explain why it's stale (e.g., "No comments, no linked PR. ~3 months stale.")
- If a linked PR exists but is also stale, note that

##### Section 3: Overall Project Progress

- One subsection per project issue, formatted as:
  ```
  ### Project #N: Title
  **Status: description, ~X% complete**
  **Goal:** one-liner from the project issue body
  **What's done:** (bulleted list of closed issues/merged PRs)
  **What's in progress:** (bulleted list of open PRs and assigned issues)
  **What's not started:** (bulleted list of unassigned stories)
  **Assessment:** (paragraph with overall evaluation)
  ```
- Include notable epics as sub-projects if they have significant scope

**Important:** Do not invent any details. Every claim must be backed by data from the fetched issues/PRs. Cite issue and PR numbers with links.

#### Step 8: Save and publish the report

1. **Get today's date:**
   ```bash
   DATE=$(date +%Y-%m-%d)
   ```

2. **Save the report:**
   Write the report to `reports/$DATE-status-report.md` using the Write tool. Create the `reports/` directory if it doesn't exist.

3. **Print a summary** to the conversation: a brief version (2–3 paragraphs) highlighting key findings, blockers, and stale items.

4. **Commit and open a draft PR:**
   ```bash
   DATE=$(date +%Y-%m-%d)
   BRANCH="reports/$DATE-status-report"
   git checkout -b "$BRANCH"
   git add "reports/$DATE-status-report.md"
   git commit -m "Add $DATE software design cycle status report"
   git push -u origin "$BRANCH"
   gh pr create --draft --title "Status Report: $DATE" --body "Auto-generated software design cycle status report for $DATE."
   ```

5. **Return the PR URL** to the user.

---

### /stale-prs

Find and report stale PRs across all linked implementation repos in the waterloo-rocketry organization.

**Trigger:** User runs `/stale-prs`

#### Step 1: Fetch open PRs from all linked repos

```bash
REPOS=(
  "omnibus"
  "omnibus-DAQms"
  "omnibus-avionics-testing-app"
  "omnibus-ts"
  "parsley"
  "parsley-ts"
  "website-react"
  "daq-raspi-deploy"
)

for REPO in "${REPOS[@]}"; do
  echo "=== $REPO ==="
  gh pr list --repo "waterloo-rocketry/$REPO" --state open \
    --json number,title,url,updatedAt,createdAt,author,reviewDecision,isDraft,additions,deletions
done
```

#### Step 2: Identify stale PRs

A PR is **stale** if it is open and its `updatedAt` is **more than 21 days ago**. Categorize by severity:

- **Critical (60+ days):** Likely abandoned. Should be closed or reassigned.
- **Warning (30–59 days):** At risk. Needs a ping or review.
- **Attention (21–29 days):** Approaching staleness. Flag for awareness.

Also flag PRs with `CHANGES_REQUESTED` review status where the author has not responded in 14+ days.

#### Step 3: Check for superseded PRs

For each stale PR, check if a newer PR exists in the same repo that addresses the same issue:

```bash
# For each stale PR, read its body to find linked issue numbers
gh pr view $PR_NUMBER --repo "waterloo-rocketry/$REPO" --json body,title --jq '.body' | grep -oE '#[0-9]+' | head -5
```

If a newer PR references the same issue, mark the stale PR as **likely superseded**.

#### Step 4: Fetch review request status

For each stale PR, check who was requested for review and whether they've responded:

```bash
gh pr view $PR_NUMBER --repo "waterloo-rocketry/$REPO" --json reviewRequests,reviews,latestReviews \
  --jq '{reviewRequests: [.reviewRequests[].login], reviews: [.latestReviews[] | "\(.author.login): \(.state)"]}'
```

#### Step 5: Produce the report

Output a markdown report with **3 sections**:

##### Section 1: Stale PRs Summary Table

Present as a markdown table sorted by staleness (oldest first):

```
| Repo | PR | Author | Title | Last Updated | Days Stale | Review Status | Notes |
|------|----|--------|-------|-------------|------------|---------------|-------|
```

In the Notes column, include:
- Whether it's a draft
- If changes were requested but not addressed
- If it appears superseded by another PR
- Any review requests that haven't been fulfilled

##### Section 2: PRs Likely Ready to Merge

List PRs that have `APPROVED` review status and are not drafts. These are blocking on the author or maintainer to merge.

##### Section 3: Recommended Actions

For each stale PR, recommend one of:
- **Close:** If superseded, abandoned, or no longer relevant
- **Ping author:** If the PR has value but the author hasn't responded
- **Request review:** If the PR is waiting on reviewers
- **Rebase and update:** If the PR has merge conflicts or is out of date

Include specific `gh` commands the user can run to take action, e.g.:

```bash
# Close a superseded PR
gh pr close $NUMBER --repo waterloo-rocketry/$REPO --comment "Closing — superseded by #$NEW_NUMBER."

# Ping an author
gh pr comment $NUMBER --repo waterloo-rocketry/$REPO --body "@$AUTHOR — are you still working on this? Let us know if you need help or if this can be closed."
```

#### Step 6: Print results

Print the full report directly to the conversation. Do **not** save to a file or create a PR — this is an on-demand diagnostic tool.
