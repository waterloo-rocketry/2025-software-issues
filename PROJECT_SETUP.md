# GitHub Project and Label Automation Setup

## Overview
This repository has been configured with issue templates for Projects, Epics, Stories, and Tasks as outlined in the README. Additionally, automation has been set up to create project-specific labels.

## Issue Templates Created

### 1. Project Template (`.github/ISSUE_TEMPLATE/project.yml`)
- For high-level projects spanning multiple months
- Includes fields for project description, success criteria, timeline, stakeholders, dependencies, and risks
- Automatically adds "project" label

### 2. Epic Template (`.github/ISSUE_TEMPLATE/epic.yml`) 
- For goals/features taking 1-2 months
- Links back to parent projects via dropdown
- Includes user stories breakdown and acceptance criteria
- Automatically adds "epic" label

### 3. Story Template (`.github/ISSUE_TEMPLATE/story.yml`)
- For individual features taking 1-2 weeks  
- Links to parent epics
- Includes user story format and task breakdown
- Automatically adds "story" label

### 4. Task Template (`.github/ISSUE_TEMPLATE/task.yml`)
- For individual tasks taking a few hours
- Links to parent stories
- Includes task type selection (Feature/Bug/Documentation/etc.)
- Supports additional labels like "good first issue", "help wanted"
- Automatically adds "task" label

## Automated Project Labels

A GitHub workflow should be created to automatically generate `project-projectname` labels when project issues are created. Due to permissions, the workflow file needs to be added manually.

### Workflow File: `.github/workflows/auto-project-labels.yml`

```yaml
name: Auto-create Project Labels

on:
  issues:
    types: [opened, edited]

jobs:
  create-project-label:
    runs-on: ubuntu-latest
    if: contains(github.event.issue.labels.*.name, 'project')
    
    steps:
      - name: Extract project name and create label
        uses: actions/github-script@v7
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          script: |
            const issue = context.payload.issue;
            const title = issue.title;
            
            // Extract project name from title (assumes format "[PROJECT] Project Name")
            const projectMatch = title.match(/^\[PROJECT\]\s*(.+)$/i);
            if (!projectMatch) {
              console.log('No project name found in title format');
              return;
            }
            
            const projectName = projectMatch[1].trim();
            const labelName = `project-${projectName.toLowerCase().replace(/\s+/g, '-').replace(/[^a-z0-9-]/g, '')}`;
            const labelColor = '0366d6'; // Blue color for project labels
            const labelDescription = `Issues related to the ${projectName} project`;
            
            try {
              // Check if label already exists
              await github.rest.issues.getLabel({
                owner: context.repo.owner,
                repo: context.repo.repo,
                name: labelName
              });
              console.log(`Label ${labelName} already exists`);
            } catch (error) {
              if (error.status === 404) {
                // Label doesn't exist, create it
                await github.rest.issues.createLabel({
                  owner: context.repo.owner,
                  repo: context.repo.repo,
                  name: labelName,
                  color: labelColor,
                  description: labelDescription
                });
                console.log(`Created new label: ${labelName}`);
              } else {
                throw error;
              }
            }
            
            // Add the label to the current issue
            await github.rest.issues.addLabels({
              owner: context.repo.owner,
              repo: context.repo.repo,
              issue_number: issue.number,
              labels: [labelName]
            });
            
            console.log(`Added label ${labelName} to issue #${issue.number}`);
```

## Recommended GitHub Project Setup

Create a GitHub Project with the following views:

### 1. Projects View
- Filter: `label:project`
- Group by: Status
- Fields: Title, Status, Timeline, Stakeholders

### 2. Epics View  
- Filter: `label:epic`
- Group by: Related Project
- Fields: Title, Status, Timeline, Related Project

### 3. Stories View
- Filter: `label:story` 
- Group by: Related Epic
- Fields: Title, Status, Priority, Estimate, Related Epic

### 4. Tasks View
- Filter: `label:task`
- Group by: Task Type
- Fields: Title, Status, Priority, Estimate, Task Type, Related Story
- Additional filters for Bug (`label:bug`) and Feature (`label:feature`)

## Labels to Create Manually

Create these base labels in the repository:
- `project` (blue) - High-level projects
- `epic` (purple) - 1-2 month goals  
- `story` (green) - 1-2 week features
- `task` (yellow) - Few hour tasks
- `bug` (red) - Bug fixes
- `feature` (blue) - New features
- `good first issue` (light green) - Good for new contributors
- `help wanted` (orange) - Extra attention needed
- `urgent` (red) - Needs immediate attention
- `blocked` (gray) - Cannot proceed

Project-specific labels will be created automatically by the workflow when project issues are created.

## Usage Instructions

1. **Create a Project**: Use the Project template to define a high-level initiative
2. **Break into Epics**: Create Epic issues linked to the project  
3. **Define Stories**: Create Story issues linked to epics
4. **Create Tasks**: Break stories down into actionable tasks
5. **Label appropriately**: Use bug/feature labels for tasks as needed

The automation will ensure proper labeling and organization of the issue hierarchy.