# Frontmatter and Naming Rules

Each `SKILL.md` must start with YAML frontmatter.

Required fields:

- `name` (required)
- `description` (required)

Optional fields:

- `license`
- `compatibility`
- `metadata` (string-to-string map)

Name rules:

- 1 to 64 characters
- lowercase alphanumeric with single hyphen separators
- no leading or trailing hyphen
- no consecutive hyphens
- must match the directory name containing `SKILL.md`

Regex:
`^[a-z0-9]+(-[a-z0-9]+)*$`

Description rules:

- 1 to 1024 characters
- specific enough to guide selection
