---
description: 
globs: 
alwaysApply: false
---
# Task List Management

## Goal

To provide guidelines to the AI assistant for completing tasks, maintaining the task list, and general task implementation instructions for managing task lists in markdown files to track progress on completing a PRD.

## Task Implementation

### 1. Receive the Task List
Read the task list called $ARGUMENTS in the `/tasks` directory.

### 2. Task Completion Protocol

* Do one subtask at a time, starting with task 1.1
* When you finish each subtask, immediately mark it as completed by changing `[ ]` to `[x]`.
* If **all** subtasks underneath a parent task are now `[x]`, follow this sequence:
    - **First**: Run the full test suite (`pytest`, `npm test`, `bin/rails test`, etc.)
    - **Only if all tests pass**: Stage changes (`git add .`)
    - **Clean up**: Remove any temporary files and temporary code before committing
    - **Commit**: Use a descriptive commit message that:
      - Uses conventional commit format (`feat:`, `fix:`, `refactor:`, etc.)
      - Summarizes what was accomplished in the parent task
      - Lists key changes and additions
      - References the task number and PRD context
      - **Formats the message as a single-line command using `-m` flags**, e.g.:

        ```
        git commit -m "feat: add payment validation logic" -m "- Validates card type and expiry" -m "- Adds unit tests for edge cases" -m "Related to T123 in PRD"
        ```
* Once all the subtasks are marked completed and changes have been committed, mark the **parent task** as completed.
* Stop after each parent-task and wait for the user to authorize go-ahead to the next parent task's sub-task.
* If **all** parent tasks in the task list are now `[x]`, update the repository README.md file by:
     - Removing the template repository text if this is the first feature implemented in the codebase
     - Accurately summarizing the current codebase, including its objectives and structure.

## Task List Maintenance

### 1. Update the task list as you work

* Mark tasks and subtasks as completed (`[x]`) per the protocol above.
* Add new tasks as they emerge.

### 2. Maintain the "Relevant Files" section

* List every file created or modified.
* Give each file a one‑line description of its purpose.

## General AI Instructions

When working with task lists, the AI must:

1. Regularly update the task list file after finishing any significant work.
2. Follow the completion protocol:
   - Mark each finished **subtask** `[x]`.
   - Mark the **parent task** `[x]` once **all** its subtasks are `[x]`.
3. Add newly discovered tasks.
4. Keep "Relevant Files" accurate and up to date.
5. Before starting work, check which sub‑task is next.
6. After implementing a subtask, update the appropriate file(s) and then move on to the next subtask.
7. After implementing the last subtask under a parent task, pause and allow the user to authorize go-ahead.