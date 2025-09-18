# GitHub Project Creation Guide

## Manual Project Setup Instructions

Since GitHub Projects v2 requires organization-level permissions, here's a step-by-step guide to create the project manually:

### Step 1: Create a New Project

1. Go to the waterloo-rocketry organization page: https://github.com/waterloo-rocketry
2. Click on the "Projects" tab
3. Click "New project"
4. Choose "Team planning" template or start from scratch
5. Name it "2025 Software Issues Tracker"
6. Add description: "Project management for the 2025 software subsystem issues and tasks"

### Step 2: Configure Project Fields

Add these custom fields to your project:

1. **Status** (Single select)
   - Backlog
   - Todo
   - In Progress
   - In Review
   - Done

2. **Priority** (Single select)
   - Low
   - Medium
   - High
   - Critical

3. **Type** (Single select)
   - Project
   - Epic
   - Story
   - Task

4. **Estimate** (Number)
   - Description: "Time estimate in days"

5. **Related Project** (Text)
   - For linking epics to projects

6. **Related Epic** (Text)
   - For linking stories to epics

7. **Related Story** (Text)
   - For linking tasks to stories

### Step 3: Create Project Views

#### View 1: Projects Overview
- **Name**: "Projects"
- **Layout**: Table
- **Filter**: `label:project`
- **Group by**: Status
- **Visible fields**: Title, Status, Priority, Estimate, Assignee
- **Sort**: Priority (High to Low), then Created (Newest first)

#### View 2: Epics Board
- **Name**: "Epics"
- **Layout**: Board
- **Filter**: `label:epic`
- **Group by**: Related Project
- **Visible fields**: Title, Status, Priority, Related Project, Assignee
- **Sort**: Priority (High to Low)

#### View 3: Stories Planning
- **Name**: "Stories"
- **Layout**: Table
- **Filter**: `label:story`
- **Group by**: Related Epic
- **Visible fields**: Title, Status, Priority, Estimate, Related Epic, Assignee
- **Sort**: Priority (High to Low), then Created (Newest first)

#### View 4: Tasks Board
- **Name**: "Tasks"
- **Layout**: Board
- **Filter**: `label:task`
- **Group by**: Status
- **Visible fields**: Title, Priority, Related Story, Assignee
- **Sort**: Priority (High to Low), then Created (Newest first)

#### View 5: Bugs & Features
- **Name**: "Bugs & Features"
- **Layout**: Table
- **Filter**: `label:task AND (label:bug OR label:feature)`
- **Group by**: Type (Bug/Feature)
- **Visible fields**: Title, Status, Priority, Type, Related Story, Assignee
- **Sort**: Priority (High to Low)

### Step 4: Link Repository

1. In your project settings, go to "Manage access"
2. Add the `waterloo-rocketry/2025-software-issues` repository
3. Enable automatic item addition for new issues with specific labels

### Step 5: Set Up Automation

Configure these automations in Project Settings > Workflows:

1. **Auto-add new issues**
   - When: Issue is created
   - If: Issue has label `project`, `epic`, `story`, or `task`
   - Then: Add to project

2. **Auto-set type field**
   - When: Item is added to project
   - If: Issue has label `project`
   - Then: Set Type field to "Project"
   - (Repeat for epic, story, task labels)

3. **Move to Done**
   - When: Issue is closed
   - Then: Set Status to "Done"

4. **Move to In Progress**
   - When: Issue is assigned
   - Then: Set Status to "In Progress"

## Project URL

Once created, the project will be available at:
`https://github.com/orgs/waterloo-rocketry/projects/[PROJECT_NUMBER]`

## Quick Setup Checklist

- [ ] Create new project in waterloo-rocketry organization
- [ ] Add custom fields (Status, Priority, Type, Estimate, Related Project/Epic/Story)
- [ ] Create 5 views: Projects, Epics, Stories, Tasks, Bugs & Features
- [ ] Link 2025-software-issues repository
- [ ] Set up automations for auto-adding and status updates
- [ ] Test with a sample issue from each type

## Integration with Issue Templates

The issue templates are already configured to:
- Automatically apply appropriate labels (project, epic, story, task)
- Include dropdowns for linking related items
- Set proper priority levels
- Include task type selection (Feature/Bug/etc.)

When you create issues using the templates, they should automatically appear in the appropriate project views based on their labels and be ready for project management workflows.

## Recommended Workflow

1. **Start with Projects**: Create high-level project issues to define major initiatives
2. **Break into Epics**: Create epic issues linked to projects for 1-2 month goals  
3. **Define Stories**: Create story issues linked to epics for 1-2 week features
4. **Create Tasks**: Break stories into actionable tasks with bug/feature types
5. **Use Project Views**: 
   - Use Projects view for high-level planning
   - Use Epics board for sprint planning
   - Use Stories table for feature planning
   - Use Tasks board for daily work management
   - Use Bugs & Features view for maintenance work

This setup provides a complete agile project management workflow aligned with the issue hierarchy defined in the templates!