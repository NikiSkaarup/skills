---
name: skill-making
description: Create compliant skills with correct paths, defaults, and frontmatter.
---

## Purpose
Help create new skills that follow path, discovery, and frontmatter rules.

## Required First Question
Ask: Where should this skill live (current directory, Claude, or OpenCode)?
Recommended default: current directory path `<name>/SKILL.md` unless the user asks for discoverable locations.

## When to Use
Use when the user wants to create or update skills and needs correct structure.

## Workflow
- Confirm target path (current directory or discoverable Claude/OpenCode paths).
- Validate `name` and `description` requirements.
- If discoverable, direct the user to the correct reference doc for the chosen target.
- If current directory, follow the current-directory default reference.

## References
- `references/current-directory-default.md`
- `references/claude-paths.md`
- `references/opencode-paths.md`
- `references/frontmatter-and-naming.md`
- `references/discovery-and-permissions.md`
- `references/examples.md`
