```markdown
# nezha Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `nezha` TypeScript codebase. You'll learn how to structure files, write imports and exports, follow commit message standards, and organize tests. These patterns help maintain consistency and quality across the project.

## Coding Conventions

### File Naming
- Use **PascalCase** for file names.
  - Example: `MyComponent.ts`, `UserService.ts`

### Import Style
- Use **relative imports** for referencing other files.
  - Example:
    ```typescript
    import { UserService } from './UserService';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // UserService.ts
    export function getUser(id: string) { ... }
    ```

### Commit Messages
- Follow **Conventional Commits** with `fix` and `feat` prefixes.
  - Example:
    ```
    feat: add user authentication middleware
    fix: correct typo in UserService
    ```

## Workflows

### Creating a New Feature
**Trigger:** When adding new functionality  
**Command:** `/new-feature`

1. Create a new file using PascalCase (e.g., `NewFeature.ts`).
2. Implement the feature using TypeScript.
3. Use relative imports for dependencies.
4. Export functions or classes using named exports.
5. Write a test file named `NewFeature.test.ts`.
6. Commit changes with a message like:  
   `feat: add NewFeature for advanced processing`

### Fixing a Bug
**Trigger:** When resolving a bug  
**Command:** `/fix-bug`

1. Locate the relevant file(s).
2. Apply the fix.
3. Update or add tests in the corresponding `.test.ts` file.
4. Commit changes with a message like:  
   `fix: resolve issue with UserService initialization`

### Writing Tests
**Trigger:** When adding or updating tests  
**Command:** `/write-test`

1. Create or update a test file matching `*.test.ts`.
2. Write test cases for the target functionality.
3. Run tests using the project's test runner (framework unknown).
4. Commit with a message like:  
   `test: add tests for UserService`

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
  - Example: `UserService.test.ts`
- The testing framework is not specified; follow existing test patterns in the codebase.
- Place test files alongside or near the files they test.

**Example:**
```typescript
// UserService.test.ts
import { getUser } from './UserService';

describe('getUser', () => {
  it('should return user data for a valid ID', () => {
    // test implementation
  });
});
```

## Commands
| Command        | Purpose                                 |
|----------------|-----------------------------------------|
| /new-feature   | Scaffold a new feature implementation   |
| /fix-bug       | Guide for fixing a bug                  |
| /write-test    | Steps for adding or updating tests      |
```
