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

### 5. **Execute Task List and Track Progress:**  
In Claude Code, run
```bash
/develop-notebook [your-notebook-name].md
```
In Cursor, Windsurf or VSCode AI chat windows, make sure `[your-notebook-name].md` and `develop-notebook.md` are in the context window, and type
```markdown
Develop a notebook based on [your-notebook-name].md using instructions in develop-notebook.md
```
The AI will execute blocks (parents) of tasks autonomously, and will check in with you once it completes a full parent task block.  If you'd like the AI to check in with you after each subtask (more human control), simply edit the `.claude\commands\process-tasks.md` file.

## Directory Structure

- `/notebooks` — Jupyter notebooks and their purpose documentation
- `/data` — Data files (raw and processed)
- `/src` — Reusable Python modules and utilities
- `.claude/commands` — AI assistant workflow guidance
- `CLAUDE.md` — Coding and collaboration standards
- `LICENSE` — MIT License

## Best Practices

1. **Documentation:**
   - Clear notebook purpose documentation
   - Well-commented code
   - Markdown cells explaining analysis steps
   - Results interpretation

2. **Data Handling:**
   - Raw data preservation
   - Reproducible preprocessing
   - Intermediate result storage
   - Clear data versioning

3. **Code Organization:**
   - Modular functions in `/src`
   - Clean, readable notebook cells
   - Proper error handling
   - Memory management

4. **Version Control:**
   - Clear commit messages
   - Regular checkpoint commits
   - `.gitignore` for data and outputs
   - Notebook output cleaning before commits

## Contributing

Contributions to this template are welcome! To contribute:

1. Fork the repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

Focus areas for contribution:
- Workflow improvements
- New utility functions
- Documentation enhancements
- Best practice additions

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