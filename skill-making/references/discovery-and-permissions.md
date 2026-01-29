# Discovery and Permissions

Discovery:

- The system walks up from the current directory to the git worktree root.
- It loads matching skills from `.opencode/skills/*/SKILL.md` and `.claude/skills/*/SKILL.md`.
- Global skills are also loaded from `~/.config/opencode/skills/*/SKILL.md` and `~/.claude/skills/*/SKILL.md`.

Permissions (OpenCode):

- Configure in `opencode.json` using pattern-based rules.
- `allow` loads immediately, `deny` hides the skill, `ask` requires approval.

Disable skills per agent:

- In custom agent frontmatter, set `tools: { skill: false }`.
- In `opencode.json`, set `agent.<name>.tools.skill` to `false`.
