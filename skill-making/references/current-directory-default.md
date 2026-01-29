# Current Directory Default

Default path:

- Use `<cwd>/<name>/SKILL.md` when the user does not request a discoverable path.
- This is intended for repo-local skills used in multiple projects.

Notes:

- The current directory path is not auto-discovered by Claude or OpenCode.
- For discoverable skills, use `.claude/skills/<name>/SKILL.md` or `.opencode/skills/<name>/SKILL.md`.
- Ensure the `name` in frontmatter matches the directory name.
