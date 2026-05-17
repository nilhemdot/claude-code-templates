```markdown
# claude-code-templates Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns used in the `claude-code-templates` repository, a TypeScript codebase built on the Express framework. You'll learn about file naming, import/export conventions, commit practices, and how to manage dependencies across multiple packages using standardized workflows.

## Coding Conventions

### File Naming
- **Style:** kebab-case
- **Example:**  
  ```
  user-controller.ts
  api-routes.ts
  ```

### Import Style
- **Relative imports** are used throughout the codebase.
- **Example:**
  ```typescript
  import { getUser } from './user-service';
  ```

### Export Style
- **Named exports** are preferred.
- **Example:**
  ```typescript
  // user-service.ts
  export function getUser(id: string) { ... }
  ```

### Commit Patterns
- **Conventional commits** are used.
- **Prefix:** `chore` (e.g., `chore: update dependencies`)
- **Average message length:** 77 characters

## Workflows

### Multi-Package Dependency Upgrade
**Trigger:** When you need to keep dependencies up-to-date across all packages/directories in the repository.  
**Command:** `/upgrade-all-dependencies`

1. Identify outdated dependencies in each `package.json`.
2. Update `package.json` and `package-lock.json` files in each affected directory.
3. Commit all updated files together, often with a detailed changelog in the commit message.

**Files involved:**
- `*/package.json`
- `*/package-lock.json`
- `package.json`
- `package-lock.json`

**Frequency:** ~2-4 times per month

**Example commit message:**
```
chore: upgrade dependencies in all packages

- Updated express to 4.18.2 in packages/api
- Updated typescript to 5.2.0 in root
```

## Testing Patterns

- **Test file pattern:** `*.test.*`
- **Testing framework:** Not explicitly detected; check for files like `user-controller.test.ts`.
- **Example:**
  ```typescript
  // user-controller.test.ts
  import { getUser } from './user-controller';

  describe('getUser', () => {
    it('returns a user object', () => {
      // test implementation
    });
  });
  ```

## Commands

| Command                   | Purpose                                                      |
|---------------------------|--------------------------------------------------------------|
| /upgrade-all-dependencies | Upgrade all dependencies across packages in the repository   |
```
