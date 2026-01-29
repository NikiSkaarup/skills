# OpenCode Skill Paths

OpenCode skills are discovered from these locations:

- Project: `.opencode/skills/<name>/SKILL.md`
- Global: `~/.config/opencode/skills/<name>/SKILL.md`

Discovery notes:

- For project-local paths, the system walks up from the current directory to the git worktree root and loads matching skills.
