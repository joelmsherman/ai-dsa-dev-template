# Data Science & Analytics Project Template

This template repository provides a structured approach for developing data science and analytics projects using Jupyter notebooks. It focuses on clear documentation, reproducible analysis, and best practices for data science workflows.

## Claude Code-Ready

The template is designed to work seamlessly with Claude Code slash commands for automated notebook creation. However, all processes and conventions can be used with GitHub Copilot, Cursor, or other agentic AI coding assistants, even if you do not use Claude Code.

## Key Features

- **Notebook-Driven Development:**  
  Use the `/requirements` directory to specify new notebook requirements as `[notebook-name].md` files. Each notebook is developed through a clear process, from initial specification to implementation.

- **Automated Workflow:**  
  The `.claude/commands/develop-notebook.md` provides comprehensive guidance for notebook development, from initial planning to execution and documentation.

- **Data Management:**  
  Organized data handling with dedicated `/data` directory for source data and processed datasets.

- **Code Quality:**  
  The `CLAUDE.md` file outlines coding standards, best practices, and guidelines specific to data science projects.

- **Reusable Components:**  
  The `/src` directory contains reusable Python modules and utility functions.

- **Open Source License:**  
  Licensed under the MIT License (see `LICENSE`).

## How to Use
First, click the green button in the upper right corner of GitHub "Use this template" > "Create a new repository", then proceed:

### 1. **Set up CLAUDE.md:**  
If you're using Claude Code, update `CLAUDE.md` to fit the parameters of your project.  This is a good starting template though and should yield good results.

### 2. **Add a Notebook Requirement:**  
Copy the template file `notebook-name.md` in `/requirements` , give it a name (like `your-notebook-name.md`), and input your requirements. It helps to be as detailed as possible when describing the objective and requirements of the notebook.  Include data sources, required libraries and other items suggested in the template file.

### 3. **Execute Task List and Track Progress:**  
In Claude Code, run
```bash
/develop-notebook [your-notebook-name].md
```
In Cursor, Windsurf or VSCode AI chat windows, make sure `[your-notebook-name].md` and `develop-notebook.md` are in the context window, and type
```markdown
Develop a notebook based on [your-notebook-name].md using instructions in develop-notebook.md
```

## Directory Structure

- `.claude/commands` — AI assistant workflow guidance
- `/data` — Data files (raw and processed)
- `/notebooks` — Jupyter notebooks and their purpose documentation
- `/requirements` — Notebook requirement files
- `/src` — Reusable Python modules and utilities
- `CLAUDE.md` — Coding and collaboration standards
- `dependencies.txt` — Codebase dependencies
- `LICENSE` — MIT License

## How to Contribute

Contributions to this template are welcome! The most impactful way to contribute is by improving the context engineering file in `.claude/commands`, which defines the automation and workflow logic for notebook development:

- `develop-notebook.md` — Guides the planning and development of notebooks.

### Pull Requests

1. **Fork the repository** and create a new branch for your changes.
2. **Edit the relevant `.md` files** in `.claude/commands` to improve instructions, add new automation logic, or clarify existing steps.
3. **Test your changes** by running through the workflow with a sample feature to ensure your edits improve the process and do not break existing conventions.
4. **Submit a pull request** with a clear description of your changes and the reasoning behind them.
5. **Engage in code review** — maintainers may ask clarifying questions or request further improvements.

All contributions should maintain clarity, consistency, and be well-documented. If you are proposing a major change, please open an issue first to discuss what you would like to change.

## Acknowledgements