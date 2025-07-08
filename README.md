# AI App Dev Template

This template repository provides a structured template for developing AI-powered applications, with a focus on clear requirements, robust task management, and best practices for code quality and collaboration. It is designed for teams or individuals building AI applications who want a repeatable, high-quality workflow from idea to implementation. 

## Claude Code-Ready

The template is designed to work seamlessly with Claude Code slash commands for automated PRD and task generation, feature management, and workflow automation. However, all processes and conventions can be used with GitHub Copilot, Cursor, or other agentic AI coding assistants, even if you do not use Claude Code.

## Key Features

- **Feature-Driven Development:**  
Use the `/features` directory to specify new features as `[feature-name].md` files. Each feature is developed through a clear process, from initial specification to implementation.

- **Automated PRD, Task Generation and Execution:**  
The `.claude/commands` directory contains markdown-based automation rules for generating Product Requirements Documents (PRDs), detailed task lists, and task execution from feature specs, ensuring clarity and traceability.

- **Task List Management:**  
Guidelines and protocols for managing and completing tasks are provided, including conventions for marking progress, running tests, and updating documentation. 

- **Coding Standards:**  
The `CLAUDE.md` file outlines coding standards, security practices, and collaboration guidelines to ensure high-quality, maintainable code.

- **Open Source License:**  
Licensed under the MIT License (see `LICENSE`).

## How to Use
First, click the green button in the upper right corner of GitHub "Use this template" > "Create a new repository", then proceed:

### 1. **Set up CLAUDE.md:**  
If you're using Claude Code, update `CLAUDE.md` to fit the parameters of your project.  This is a good starting template through and should yield good results.

### 2. **Add a Feature:**  
Create a new markdown file in `/features` , like `[feature-name].md` describing your feature. It helps to be as detailed as possible when describing the feature.  Include example coding snippets, and URLs to documentation along with why the URL is important for implementing the feature.

### 3. **Generate PRD from Feature file:**  
In Claude Code, run 
```bash
/create-prd [feature-name].md
```
In Cursor, Windsurf or VSCode AI chat windows, make sure `[feature-name].md` and `create-prd.md` are in the context window, and type
```markdown
Create a PRD for the feature described in [feature-name].md using instructions provided in create-prd.md 
```
### 4. **Generate Task List from PRD:**
In Claude Code, run 
```bash
/generate-tasks [prd-feature-name].md
```
In Cursor, Windsurf or VSCode AI chat windows, make sure `[prd-feature-name].md` and `generate-tasks.md` are in the context window, and type
```markdown
Create a task list for the PRD described in [prd-feature-name].md using instructions provided in generate-tasks.md 
```
### 5. **Execute Task List and Track Progress:**  
In Claude Code, run
```bash
/process-tasks [tasks-prd-feature-name].md
```
In Cursor, Windsurf or VSCode AI chat windows, make sure `[tasks-prd-feature-name].md` and `process-tasks.md` are in the context window, and type
```markdown
Execute tasks, starting with task 1.1, in [tasks-prd-feature-name].md using instructions provided in process-tasks.md 
```
The AI will execute blocks (parents) of tasks autonomously, and will check in with you once it completes a full parent task block.  If you'd like the AI to check in with you after each subtask (more human control), simply edit the `.claude\commands\process-tasks.md` file.

## Directory Structure

- `/features` — Feature specifications  
- `/prds` — Product Requirements Documents (generated)  
- `/tasks` — Task lists (generated)  
- `.claude/commands` — Automation rules for Claude or other AI assistants  
- `CLAUDE.md` — Coding and collaboration standards  
- `LICENSE` — MIT License

## How to Contribute

Contributions to this template are welcome! The most impactful way to contribute is by improving the context engineering files in `.claude/commands`, which define the automation and workflow logic for feature development:

- `create-prd.md` — Guides the generation of Product Requirements Documents from feature specs.
- `generate-tasks.md` — Defines how to break down PRDs into actionable task lists.
- `process-tasks.md` — Outlines the protocols for executing and tracking tasks.

### Pull Requests

1. **Fork the repository** and create a new branch for your changes.
2. **Edit the relevant `.md` files** in `.claude/commands` to improve instructions, add new automation logic, or clarify existing steps.
3. **Test your changes** by running through the workflow with a sample feature to ensure your edits improve the process and do not break existing conventions.
4. **Submit a pull request** with a clear description of your changes and the reasoning behind them.
5. **Engage in code review** — maintainers may ask clarifying questions or request further improvements.

All contributions should maintain clarity, consistency, and be well-documented. If you are proposing a major change, please open an issue first to discuss what you would like to change.

## Acknowledgements

Special thanks to the following individuals for their foundational ideas and inspiration:

- [Ryan Carson](https://github.com/snarktank/ai-dev-tasks) — for the three-part context engineering concept.
- [Cole Medin](https://github.com/coleam00/context-engineering-intro) — for ideas and examples on integrating Claude slash commands.
- And others in the open source AI developer community who have contributed to the evolution of agentic workflows and context engineering.