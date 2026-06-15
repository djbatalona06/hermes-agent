```markdown
# hermes-agent Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns, conventions, and workflows used in the `hermes-agent` Swift codebase. It covers file naming, import/export styles, commit conventions, and testing patterns to ensure consistency and maintainability in your contributions.

## Coding Conventions

### File Naming
- Use **PascalCase** for all file names.
  - **Example:** `HermesAgent.swift`, `NetworkManager.swift`

### Import Style
- Use **relative imports** for referencing other modules or files.
  - **Example:**
    ```swift
    import ../Utilities/Logger
    ```

### Export Style
- Use **named exports** to expose specific classes, structs, or functions.
  - **Example:**
    ```swift
    public class HermesAgent {
        // ...
    }
    ```

### Commit Patterns
- Commit messages are **freeform** (no strict prefix), typically concise (average 49 characters).
  - **Example:**  
    ```
    Fix agent reconnection logic on network failure
    ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new capability or module  
**Command:** `/add-feature`

1. Create a new file using PascalCase (e.g., `NewFeature.swift`).
2. Use relative imports to reference dependencies.
3. Export new classes or functions using named exports.
4. Write corresponding tests in a `.test.swift` file.
5. Commit changes with a concise, descriptive message.

### Fixing a Bug
**Trigger:** When resolving a defect or unintended behavior  
**Command:** `/fix-bug`

1. Locate the relevant file(s) and make necessary code changes.
2. Update or add tests in the corresponding `.test.swift` file.
3. Commit with a clear message describing the fix.

### Writing Tests
**Trigger:** When adding or updating tests for code  
**Command:** `/write-test`

1. Create or update a test file matching the pattern `*.test.swift`.
2. Write tests for public interfaces and edge cases.
3. Run tests using the project's test runner (framework unknown).

## Testing Patterns

- Test files follow the pattern: `*.test.swift`
  - **Example:** `HermesAgent.test.swift`
- The testing framework is not specified; use the project's standard runner.
- Place tests alongside or near the code they cover.
- Cover both expected and edge-case behaviors.

## Commands
| Command      | Purpose                                 |
|--------------|-----------------------------------------|
| /add-feature | Scaffold and document a new feature     |
| /fix-bug     | Guide steps to fix a bug                |
| /write-test  | Steps for writing or updating tests     |
```
