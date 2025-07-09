---
description: 
globs: 
alwaysApply: false
---
# Rule: Generate a Jupyter notebook from a detailed requirements file

## Goal

To guide an AI assistant in planning, developing and executing data science notebooks in Jupyter, based on a user requirements file `notebook-name.md` specification in the `/requirements` directory.  The AI should run the plan for each cell in the notebook by the user before executing the code.  

## Process

### 1. Receive and Analyze the Notebook Requirements
Read the requirements file called $ARGUMENTS in the `/requirements` directory.

### 2. Ask Clarifying Questions
Before planning and developing the notebook, the AI *must* ask clarifying questions to gather sufficient detail. The goal is to understand the "what" and "why" of the notebook, not necessarily the "how". Make sure to provide options in letter/number lists so I can respond easily with my selections.

#### 2.1 Examples of clarifying questions
The AI should adapt its questions based on the prompt, but here are some common areas to explore:

* Data availability and format
* Specific analysis techniques required
* Expected visualization types
* Success criteria
* Resource constraints
* Output format requirements

### 3. Generate Development Plan
Based on the initial prompt and the user's answers to the clarifying questions, ULTRATHINK about the development plan for the notebook. Consider:

#### 3.1 Data Processing Steps
- Data loading and validation
- Cleaning and preprocessing
- Feature engineering

#### 3.2 Analysis Components
- Exploratory data analysis (EDA)
- Statistical analysis
- Model development
- Visualization creation

#### 3.3 Output Generation
- Results compilation
- Visualization formatting
- Documentation requirements

#### 3.4 Quality Checks
- Data validation steps
- Analysis validation
- Results verification

### 4. Notebook Development
Now create the Jupyter notebook following these guidelines:

#### 4.1 Development and Execution Protocol
* Develop and execute notebook cells sequentially, making sure to run then in order. Verify each cell's output and document issues.
* Catch, log and fix errors that arise.
* Review all results by validating outputs, checking visualizations and verifying analysis results.

#### 4.2 Structure
* Write clear section headers with markdown.
* Organize code cells and keep each cell focused and single-purpose.
* Use inline documentation where appropriate.
* Manage output cells appropriately.

#### 4.3 Code Quality
* Follow PEP 8 Style and standard data science patterns.
* Use modular functions.
* Implement error handling.
* Structure code for peformance and memory management.

#### 4.4 Output Management
* Format visualizations using a clean, modern themes
* Style all tables consistently
* Convert any intermediate Pandas dataframes to Spark dataframes prior to writing back to lakehouse.
* Save intermediate data if needed.

#### 4.5 Documentation
* Use markdown cells to explain the purpose of blocks of code cells.
* Use markdown to document code assumptions and limitations.
* Use markdown explain and reference libraries used in the notebook.
* Use inline comments for complicated portions of code.
  
### 5. Save the Notebook
Save the generated Jupyter notebook file using the following specification:

* **Format:** Jupyter notebook (`.ipynb`)
* **Location:** `/notebooks/`
* **Filename:** `notebook-$ARGUMENTS.md`

For example, if the notebook requirements file in the `requirements` directory was `my-notebook-name.md`, then the saved notebook file should be named `notebook-my-notebook-name.md`.

## Final Instructions

Do NOT start building the notebook until you have asked the user clarifying questions. Take the user's answers to the clarifying questions and improve the notebook plan and development.

