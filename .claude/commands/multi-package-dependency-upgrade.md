---
name: multi-package-dependency-upgrade
description: Workflow command scaffold for multi-package-dependency-upgrade in claude-code-templates.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /multi-package-dependency-upgrade

Use this workflow when working on **multi-package-dependency-upgrade** in `claude-code-templates`.

## Goal

Updates dependencies across multiple package.json/package-lock.json files in a monorepo, often as part of an automated process (e.g., Dependabot).

## Common Files

- `*/package.json`
- `*/package-lock.json`
- `package.json`
- `package-lock.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify outdated dependencies in each package (package.json).
- Update package.json and package-lock.json files in each affected directory.
- Commit all updated files together, often with a detailed changelog in the commit message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.