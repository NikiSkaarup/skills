---
name: skill-making
description: Create compliant OpenCode or Claude skills with correct paths and frontmatter.
---

## Purpose
Help create new skills that follow OpenCode and Claude-compatible rules.

## Required First Question
Ask: Is this skill for Claude (`.claude/skills/...`) or OpenCode (`.opencode/skills/...`)?
Recommended default: Claude unless the user specifies otherwise.

## When to Use
Use when the user wants to create or update skills and needs correct structure.

## Workflow
- Confirm target (Claude or OpenCode) before giving path guidance.
- Validate `name` and `description` requirements.
- Direct the user to the correct reference doc for the chosen target.

## References
- `references/claude-paths.md`
- `references/opencode-paths.md`
- `references/frontmatter-and-naming.md`
- `references/discovery-and-permissions.md`
- `references/examples.md`
