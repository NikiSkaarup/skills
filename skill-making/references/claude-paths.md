# Claude Skill Paths

Claude-compatible skills are discovered from these locations:

- Project: `.claude/skills/<name>/SKILL.md`
- Global: `~/.claude/skills/<name>/SKILL.md`

Discovery notes:

- For project-local paths, the system walks up from the current directory to the git worktree root and loads matching skills.
