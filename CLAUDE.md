# Data Science Development Guidelines
Review this file at the start of every conversation.

## 1. Basic Rules
- First understand the analysis objectives and available data before starting any code.
- Keep analysis steps clear, documented, and reproducible.
- Focus on creating meaningful insights and visualizations.

## 2. Coding Standards
- Use Python as the primary language
- Follow data science best practices and patterns
- Write clean, efficient, and well-documented code
- Use descriptive variable names that reflect the data they contain
- Include markdown cells explaining analysis steps

## 3. Data Handling
- Always preserve raw data - never modify original data files
- Document data cleaning and preprocessing steps
- Handle missing data appropriately and document the approach
- Implement proper data validation and quality checks
- Consider memory usage with large datasets

## 4. Analysis Development
- Start with exploratory data analysis (EDA)
- Document assumptions and limitations
- Include statistical justification for methods used
- Create clear, informative visualizations
- Save intermediate results when appropriate

## 5. Security & Privacy
- Never commit sensitive data to the repository
- Remove or mask any personally identifiable information (PII)
- Use environment variables for sensitive configuration
- Document any data access requirements or restrictions

## 6. Collaboration
- Write clear, comprehensive markdown documentation
- Use consistent notebook structure and formatting
- Document dependencies and environment setup
- Make analyses reproducible by others
- Keep notebook outputs clean in version control

## 7. Quality Assurance
- Validate data transformations
- Include sanity checks for calculations
- Test critical functions in /src
- Document edge cases and limitations
- Include error handling for data processing

## 8. Dependencies
- Use standard data science libraries (pandas, numpy, scikit-learn, etc.)
- Document all requirements in requirements.txt
- Keep track of package versions for reproducibility
- Prefer stable, well-maintained packages