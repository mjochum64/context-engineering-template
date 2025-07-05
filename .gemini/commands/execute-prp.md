# Execute PRP for Gemini

## PRP file: $ARGUMENTS

Your task is to implement the feature described in the provided Product Requirements Prompt (PRP) file. You must follow the instructions within the PRP with extreme precision to ensure a successful, one-pass implementation.

## Execution Process

1.  **Full Context Ingestion**:
    *   Before writing any code, read the **entire** PRP file (`$ARGUMENTS`) from top to bottom.
    *   Internalize the `Goal`, all items in `All Needed Context`, the `Implementation Blueprint`, and the `Validation Loop`. You must have a complete picture before starting.

2.  **Follow the Blueprint**:
    *   The `Implementation Blueprint` is your step-by-step guide. Execute the tasks in the exact order they are listed.
    *   Adhere strictly to the specified file modifications (`CREATE`, `MODIFY`, `INJECT`, etc.).
    *   Use the provided `pseudocode` and `patterns` as the ground truth for your implementation logic.

3.  **Implement and Validate (The Loop)**:
    *   For each task or logical chunk of code you write, immediately run the corresponding validation commands from the `Validation Loop` section of the PRP (e.g., linting, type-checking, unit tests).
    *   **CRITICAL**: If a validation command fails, do not proceed. Analyze the error output, debug the code you just wrote, apply a fix, and re-run the validation command.
    *   Repeat this "code -> test -> fix" cycle until all validation steps for the current task pass.

4.  **Adhere to Global Rules**:
    *   Throughout the entire process, you must follow all rules and conventions defined in the `GEMINI.md` file. This includes file structure, naming, testing standards, and code style.

5.  **Final Verification**:
    *   Once all implementation tasks are complete and have passed their individual validation steps, perform the final, full-project validation as described in the PRP's `Final validation Checklist`.
    *   Ensure all criteria are met before considering the task complete.

## Output

Your final output should be the new and modified files as requested by the PRP. Do not provide summaries or explanations unless the PRP explicitly asks for them. The code is the deliverable.

Remember: The PRP is designed to give you all the context you need. Trust the blueprint. Validate your work at every step.