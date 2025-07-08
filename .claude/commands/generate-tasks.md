---
description: 
globs: 
alwaysApply: false
---
# Rule: Generate a Task List from a PRD

## Goal

To guide an AI assistant in creating a detailed, step-by-step task list in Markdown format based on an existing Product Requirements Document (PRD) `prd-[feature-name].md` located in the `/prds` directory. The task list should guide a developer through implementation.

## Process

### 1. Receive and Analyze the PRD
Read the PRD called $ARGUMENTS in the `/prds` directory.

### 2. Generate Parent Tasks
Based on the PRD analysis, create the file and generate the main, high-level tasks required to implement the feature. Use your judgement on how many high-level tasks to use, but try to shoot for about 5. Present these tasks to me in the specified format (without sub-tasks yet). Inform the user: "I have generated the high-level tasks based on the PRD. Ready to generate the sub-tasks? Respond with 'Go' to proceed."

### 3. Wait for Confirmation
Pause and wait for the user to respond with "Go".

### 4. Generate Sub-Tasks
Once the user confirms, break down each parent task into smaller, actionable sub-tasks necessary to complete the parent task. Ensure sub-tasks logically follow from the parent task and cover the implementation details implied by the PRD.

### 5. Identify Relevant Files
Based on the tasks and PRD, identify potential files that will need to be created or modified. List these under the `Relevant Files` section, including corresponding test files if applicable. Unit test files should typically be placed alongside the code files they are testing (e.g., `MyComponent.tsx` and `MyComponent.test.tsx` in the same directory).

### 6. Generate the Task List
ULTRATHINK when combining the parent tasks, sub-tasks and relevant files into the final Markdown structure. Generate the task list using the structure outlined below. Be mindful of the target audience described below. Next to each sub-task, estimate the time (approx. human hrs) it would take an average human junior developer to implement the task.

#### Task List Structure
The generated task list must follow this structure:

```markdown
# Tasks
- [ ] 1.0 Parent Task Title
  - [ ] 1.1 [Sub-task description 1.1] - approx. human hrs
  - [ ] 1.2 [Sub-task description 1.2] - approx. human hrs
- [ ] 2.0 Parent Task Title
  - [ ] 2.1 [Sub-task description 2.1] - approx. human hrs
- [ ] 3.0 Parent Task Title (may not require sub-tasks if purely structural or configuration)

# Relevant Files
- `path/to/potential/file1.ts` - Brief description of why this file is relevant (e.g., Contains the main component for this feature).
- `path/to/file1.test.ts` - Unit tests for `file1.ts`.
- `path/to/another/file.tsx` - Brief description (e.g., API route handler for data submission).
- `path/to/another/file.test.tsx` - Unit tests for `another/file.tsx`.
- `lib/utils/helpers.ts` - Brief description (e.g., Utility functions needed for calculations).
- `lib/utils/helpers.test.ts` - Unit tests for `helpers.ts`.
```

#### Task List Audience
Assume the primary reader of the task list is a **junior developer** who will implement the feature.

### 7. Save the Task List
Save the generated document using the following specification:

* **Format:** Markdown (`.md`)
* **Location:** `/tasks/`
* **Filename:** `tasks-$ARGUMENTS.md`

For example, if the PRD file name in the `prds` directory was `prd-my-awesome-feature.md`, then the saved task list file should be named `tasks-prd-my-awesome-feature.md`.

## Final Instructions

Pause after generating parent tasks to get user confirmation ("Go") before proceeding to generate the detailed sub-tasks. This ensures the high-level plan aligns with user expectations before diving into details.

