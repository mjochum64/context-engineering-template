# Create PRP for Gemini

## Feature file: $ARGUMENTS

Generate a complete PRP (Product Requirements Prompt) for the feature request. Your goal is to conduct thorough research of the codebase and external sources to create a comprehensive blueprint that an AI agent can execute successfully in one pass.

First, read the feature file (`$ARGUMENTS`) to understand the core requirements, the provided examples, and any other considerations.

The AI agent that will execute the PRP only has access to the context you provide within the PRP itself, its general knowledge, and the ability to browse the web and read files. It is critical that your research findings are included or referenced in the PRP.

## Research Process

1.  **Codebase Analysis**:
    *   Search for similar features, modules, or patterns in the current codebase.
    *   Identify key files that should be referenced as examples in the PRP.
    *   Note existing conventions (naming, structure, style) that must be followed.
    *   Analyze existing test patterns (`tests/`) to define the validation approach.

2.  **External Research**:
    *   Search for best practices related to the feature or libraries involved.
    *   Find official library documentation (and include specific URLs).
    *   Look for high-quality implementation examples (e.g., on GitHub, official blogs).
    *   Identify and document common pitfalls or "gotchas".

## PRP Generation

Use `PRPs/templates/prp_base.md` as the template for the new PRP.

### Critical Context to Include in the PRP:
-   **Documentation**: Direct URLs to specific, relevant sections of API docs.
-   **Code Examples**: Real, relevant code snippets from this codebase to enforce patterns.
-   **Gotchas**: A clear list of library quirks, version issues, or architectural constraints.
-   **Patterns**: Explicit instructions to follow existing design patterns from specific files.

### Implementation Blueprint:
-   Define a clear, step-by-step list of tasks.
-   Start with pseudocode that outlines the proposed logic and references real files/functions.
-   Include a clear error handling strategy.

### Validation Gates (Must be Executable):
-   Provide concrete, copy-pasteable commands for linting, type-checking, and running tests.

## Output
Save the final output as `PRPs/{feature-name}.md`.

## Quality Checklist & Confidence Score
-   Before finishing, double-check that all necessary context is included.
-   Ensure validation gates are executable and correct.
-   Confirm that the implementation path is clear and logical.
-   Score your confidence (1-10) that the PRP can be implemented successfully in a single attempt.

Remember: The goal is one-pass implementation success through comprehensive context.