---
name: Generic Task
about: Create a new task following project conventions
title: "TASK: "
labels: task
assignees: 
---

## Description
<!-- Describe the task clearly. Include context, objectives, and scope. -->

### Context
<!-- Why this task exists. What is the current situation? -->

### Objectives
<!-- What the task aims to achieve -->

### Scope / Actions
<!-- List actionable steps for this task -->
- [ ] Step 1
- [ ] Step 2
- [ ] Step 3

### Acceptance Criteria
<!-- Conditions to consider the task done -->
- [ ] Criteria 1
- [ ] Criteria 2
- [ ] Criteria 3

### Sub-Module / Component
<!-- Specify which sub-module this task applies to, e.g., framework -->

---

## Issue Prefix Convention
Use the following prefixes in your GitHub issue titles:

| Prefix        | Keyword         | Type                | Color    | Description                              |
|---------------|-----------------|---------------------|----------|------------------------------------------|
| `Bug`         | `BUG:`          | type: bug           | Red      | Fixes regression or broken logic         |
| `Task`        | `TASK:`         | type: task          | Blue     | General work                             |
| `Subtask`     | `SUB:`          | type: subtask       | Grey     | Smaller chunks of a larger epic          |
| `Enhancement` | `ENH:`          | type: enhancement   | Green    | Improvement to existing feature          |
| `Refactor`    | `REFACTOR:`     | type: enhancement   | yellow   | Code restructuring                       |
| `Feature`     | `FEAT:`         | type: feature       | Purple   | Brand new functionality                  |
| `Documentation`| `DOC:`         | type: documentation | Orange   | Docs changes/additions                   |

### Usage Examples
- `TASK: Upgrade Java version to 25 in framework module`
- `BUG: Fix NullPointerException in framework initialization`
- `ENH: Optimize Spotless formatting rules`
- `FEAT: Add new calculation engine`
- `DOC: Update README with Spotless setup instructions`
