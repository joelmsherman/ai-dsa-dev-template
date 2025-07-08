# Claude Rules
Review this file at the start of every conversation.

## 1. Basic Rules
- First think through the problem and read the codebase before you start writing code.
- Make every task and code change you do as simple as possible.
- The goal is one-pass implementation success through comprehensive context.
 
## 2. Coding Standards
- Use python as the primary language, where possible
- Write clean, modular, and well-documented code.
- Prefer readability and maintainability over cleverness.
- Use descriptive variable and function names.
- Follow best practices for the chosen language and framework.

## 3. Feature Development
- When adding new features, ensure they are loosely coupled and easy to test.
- Provide clear docstrings or comments explaining the purpose and usage of new modules or functions.
- If a feature requires configuration, document the necessary environment variables or settings.

## 4. Security & Privacy
- When you write code, check through it to make sure that it has no vulnerabilities that can be exploited
- Do not hardcode sensitive information (API keys, passwords, etc.).
- Follow security best practices for authentication, authorization, and data handling.

## 5. Collaboration
- Write code that is easy for others to understand and extend.
- Document any assumptions, limitations, or design decisions in code comments or in the README.
- As you develop and commit code, you must ensure the README.md file adequately documents the repo for a general audience.

## 6. Testing
- Include tests for new features where possible.
- Prefer automated tests (unit, integration) to ensure reliability.
- After updating any logic, check whether existing unit tests need to be updated. If so, do it.

## 7. Dependencies
- Use well-maintained, reputable libraries.
- Document any new dependencies in the appropriate requirements or package files.