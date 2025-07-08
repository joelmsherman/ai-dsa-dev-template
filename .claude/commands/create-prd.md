---
description:
globs:
alwaysApply: false
---
# Rule: Generate a Product Requirements Document (PRD)

## Goal

To guide an AI assistant in writing a detailed Product Requirements Document in Markdown format, based on an initial user `feature.md` specification in the `/features` directory. The PRD should be clear, actionable, and suitable for a junior developer to understand and implement the feature.

## Process

### 1. Receive and Analyze the Feature file
Read the feature file called $ARGUMENTS in the `/features` directory.

### 2. Ask Clarifying Questions
Before writing the PRD, the AI *must* ask clarifying questions to gather sufficient detail. The goal is to understand the "what" and "why" of the feature, not necessarily the "how" (which the developer will figure out). Make sure to provide options in letter/number lists so I can respond easily with my selections.

#### Examples of clarifying questions
The AI should adapt its questions based on the prompt, but here are some common areas to explore:

*   **Problem/Goal:** "What problem does this feature solve for the user?" or "What is the main goal we want to achieve with this feature?"
*   **Target User:** "Who is the primary user of this feature?"
*   **Core Functionality:** "Can you describe the key actions a user should be able to perform with this feature?"
*   **User Stories:** "Could you provide a few user stories? (e.g., As a [type of user], I want to [perform an action] so that [benefit obtained].)"
*   **Acceptance Criteria:** "How will we know when this feature is successfully implemented? What are the key success criteria?"
*   **Scope/Boundaries:** "Are there any specific things this feature *should not* do (non-goals)?"
*   **Data Requirements:** "What kind of data does this feature need to display or manipulate?"
*   **Design/UI:** "Are there any existing design mockups or UI guidelines to follow?" or "Can you describe the desired look and feel?"
*   **Edge Cases:** "Are there any potential edge cases or error conditions we should consider?"
   
### 3. Generate PRD
Based on the initial prompt and the user's answers to the clarifying questions, ULTRATHINK about the PRD, plan your approach, and generate the PRD using the structure outlined below. Be mindful of the target audience described below.

#### PRD Structure

1.  **Introduction/Overview:** Briefly describe the feature, the problem it solves, or the goal it will achieve.
2.  **Goals:** List the specific, measurable objectives for this feature.
3.  **Success Metrics:** How will the success of this feature be measured? (e.g., "Increase user engagement by 10%", "Reduce support tickets related to X").
4.  **User Stories:** Detail the user narratives describing feature usage and benefits.
5.  **Functional Requirements:** List the specific functionalities the feature must have. Use clear, concise language (e.g., "The system must allow users to upload a profile picture."). Number these requirements.
6.  **Design Considerations (Optional):** Link to mockups, describe UI/UX requirements, or mention relevant components/styles if applicable.
7.  **Technical Considerations (Optional):** Mention any known technical constraints, dependencies, or suggestions (e.g., "Should integrate with the existing Auth module").

#### PRD Target Audience
Assume the primary reader of the PRD is a **junior developer**. Therefore, requirements should be explicit, unambiguous, and avoid jargon where possible. Provide enough detail for them to understand the feature's purpose and core logic.

### 4. Save the PRD 
Save the generated document using the following specification:

*   **Format:** Markdown (`.md`)
*   **Location:** `/prds/`
*   **Filename:** `prd-$ARGUMENTS.md`

For example, if the feature file name in the `features` directory was `my-awesome-feature.md`, then the saved PRD file should be named `prd-my-awesome-feature.md`.

## Final Instructions

Do NOT start implementing the PRD until you have asked the user clarifying questions. Take the user's answers to the clarifying questions and improve the PRD.