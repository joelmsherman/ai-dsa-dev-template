# Data Science & Analytics Project Template

This template repository provides a structured approach for developing data science and analytics projects using Jupyter notebooks. It focuses on clear documentation, reproducible analysis, and best practices for data science workflows.

## AI Assistant Ready

The template is designed to work seamlessly with various AI coding assistants (like GitHub Copilot, Claude, or others) to help develop and document data science analyses. The structured workflow ensures consistency and quality across your analytics projects.

## Key Features

- **Notebook-Driven Development:**  
  Use the `/notebooks` directory to create and organize Jupyter notebooks, with each notebook having a clear purpose documented in a corresponding markdown file.

- **Automated Workflow:**  
  The `.claude/commands/notebook_workflow.md` provides comprehensive guidance for notebook development, from initial planning to execution and documentation.

- **Data Management:**  
  Organized data handling with dedicated `/data` directory for source data and processed datasets.

- **Code Quality:**  
  The `CLAUDE.md` file outlines coding standards, best practices, and guidelines specific to data science projects.

- **Reusable Components:**  
  The `/src` directory contains reusable Python modules and utility functions.

- **Open Source License:**  
  Licensed under the MIT License (see `LICENSE`).

## How to Use

1. **Create New Project:**  
   Click "Use this template" > "Create new repository" on GitHub

2. **Set Up Environment:**  
   - Create a virtual environment
   - Install required packages from `requirements.txt`
   - Configure Jupyter kernel

3. **Start a New Analysis:**  
   - Copy `notebooks/notebook_purpose.md` template
   - Fill in analysis objectives and requirements
   - Use AI assistant to help develop the notebook

4. **Development Workflow:**  
   In VS Code AI chat window, provide the notebook purpose file and notebook_workflow.md in context, then type:
   ```markdown
   Develop a notebook based on [notebook-name]_purpose.md using instructions in notebook_workflow.md
   ```

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