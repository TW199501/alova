```markdown
# alova Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `alova` TypeScript codebase. You'll learn how to name files, structure imports/exports, write conventional commits, and organize tests. This guide also provides suggested commands for common workflows to streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.ts`, `apiRequestHandler.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './fetchData';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    export function fetchData() { ... }
    export const API_URL = '...';
    ```

### Commit Messages
- Use **conventional commits** with a `chore` prefix for non-feature/bugfix changes.
  - Example:  
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Creating a New Module
**Trigger:** When adding new functionality to the codebase  
**Command:** `/new-module`

1. Create a new TypeScript file using camelCase naming.
2. Write your code using named exports.
3. Use relative imports to bring in any dependencies.
4. Add corresponding test files as needed.

### Making a Commit
**Trigger:** When committing changes  
**Command:** `/commit`

1. Write a commit message using the conventional commit format.
   - Use `chore:` for maintenance or non-feature changes.
   - Keep the message concise (around 44 characters).
2. Example:
   ```
   chore: refactor fetchData for clarity
   ```

### Writing Tests
**Trigger:** When adding or updating functionality  
**Command:** `/add-test`

1. Create a test file matching the pattern `*.test.*` (e.g., `fetchData.test.ts`).
2. Write tests for your module (testing framework is unspecified; follow project conventions).
3. Use relative imports to import the module under test.

## Testing Patterns

- Test files are named using the pattern `*.test.*` (e.g., `apiRequestHandler.test.ts`).
- The specific testing framework is not detected; follow the existing test file structure.
- Place test files alongside the modules they test or in a dedicated `tests` directory if present.

## Commands
| Command      | Purpose                                  |
|--------------|------------------------------------------|
| /new-module  | Scaffold a new module with conventions   |
| /commit      | Make a conventional commit               |
| /add-test    | Add a new test file for a module         |
```
