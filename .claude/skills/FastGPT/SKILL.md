```markdown
# FastGPT Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the FastGPT TypeScript codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to write and run tests. While no specific automation workflows were detected, this guide provides best practices and suggested commands to streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userService.ts`, `dataProcessor.test.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './apiClient';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In utils.ts
    export function parseInput(input: string): ParsedInput { ... }

    // In another file
    import { parseInput } from './utils';
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `chore` prefix for maintenance commits.
  - Example:  
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Creating a New Feature
**Trigger:** When adding new functionality to the codebase  
**Command:** `/new-feature`

1. Create a new TypeScript file using camelCase naming.
2. Use relative imports to include dependencies.
3. Export your functions or components using named exports.
4. Write corresponding test files with the `.test.ts` suffix.
5. Commit changes using the conventional commit format.

### Refactoring Code
**Trigger:** When improving or restructuring existing code  
**Command:** `/refactor`

1. Identify the code to refactor.
2. Rename files if necessary, using camelCase.
3. Update imports to maintain relative paths.
4. Ensure all exports remain named.
5. Run all relevant tests to confirm no regressions.
6. Commit with a message like:  
   ```
   chore: refactor [module] for clarity
   ```

### Writing and Running Tests
**Trigger:** When adding or updating tests  
**Command:** `/test`

1. Create test files with the `.test.ts` or `.test.js` suffix.
2. Write tests for each exported function or module.
3. Use the project's test runner to execute tests (framework unknown; check project scripts).
4. Ensure all tests pass before committing.

## Testing Patterns

- Test files are named with the pattern `*.test.*` (e.g., `apiClient.test.ts`).
- Each test file should cover the functions or modules exported from the corresponding implementation file.
- Testing framework is not specified; refer to the project's documentation or scripts for running tests.

## Commands
| Command        | Purpose                                         |
|----------------|------------------------------------------------|
| /new-feature   | Scaffold a new feature with proper conventions |
| /refactor      | Refactor code following project standards      |
| /test          | Write and run tests for your code              |
```
