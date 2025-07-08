# Notebook Development Workflow

## Goal

To guide an AI assistant in developing and executing data science notebooks based on a notebook purpose specification. This workflow combines planning, development, and execution phases into a single streamlined process.

## Process

### 1. Analyze Purpose Document

Read the notebook purpose document from the `/notebooks` directory.

### 2. Ask Clarifying Questions

Before proceeding with development, ask clarifying questions about:

- Data availability and format
- Specific analysis techniques required
- Expected visualization types
- Success criteria
- Resource constraints
- Output format requirements

### 3. Generate Development Plan

Create a structured plan that includes:

1. **Data Processing Steps**
   - Data loading and validation
   - Cleaning and preprocessing
   - Feature engineering

2. **Analysis Components**
   - Exploratory data analysis (EDA)
   - Statistical analysis
   - Model development (if applicable)
   - Visualization creation

3. **Output Generation**
   - Results compilation
   - Visualization formatting
   - Documentation requirements

4. **Quality Checks**
   - Data validation steps
   - Analysis validation
   - Results verification

### 4. Notebook Development

Create or modify the Jupyter notebook following these guidelines:

1. **Structure**
   - Clear section headers with markdown
   - Code cell organization
   - Documentation inline
   - Output cell management

2. **Code Quality**
   - Modular functions
   - Error handling
   - Performance considerations
   - Memory management

3. **Documentation**
   - Markdown explanations
   - Code comments
   - Results interpretation
   - Limitations noted

### 5. Execution Protocol

When executing notebook cells:

1. **Sequential Execution**
   - Run cells in order
   - Verify each cell's output
   - Document any issues

2. **Error Handling**
   - Catch and handle exceptions
   - Log issues
   - Implement fixes

3. **Results Review**
   - Validate outputs
   - Check visualizations
   - Verify analysis results

### 6. Completion Checklist

- [ ] All data processing steps completed
- [ ] Analysis components executed
- [ ] Visualizations generated
- [ ] Results documented
- [ ] Code commented and cleaned
- [ ] Memory usage optimized
- [ ] Outputs saved/exported
- [ ] README updated

## Guidelines for AI Assistant

1. **Cell Management**
   - Keep code cells focused and single-purpose
   - Use markdown cells for explanations
   - Clean up unnecessary outputs

2. **Documentation**
   - Explain key decisions
   - Document assumptions
   - Note limitations
   - Reference sources

3. **Best Practices**
   - Follow PEP 8 style
   - Use standard data science patterns
   - Implement memory management
   - Consider scalability

4. **Output Management**
   - Clear visualization formatting
   - Consistent table styling
   - Export key results
   - Save intermediate data if needed
