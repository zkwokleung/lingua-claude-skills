# lingua-claude-skills

A collection of [Claude Code](https://claude.com/claude-code) skills for language learners. Use Claude as a tutor, drill partner, and reference, right inside your terminal.

## Available skills

Skills are organized by language.

### Japanese

| Skill | Description |
|-------|-------------|
| [`jlpt-question`](japanese/jlpt-question/SKILL.md) | Generates a single JLPT practice question (N1–N5) with 4 multiple-choice options and grades your answer. Covers vocabulary, kanji reading/writing, grammar, and reading comprehension calibrated to the target level. |

More skills will be added over time, including additional Japanese practice modes and other languages.

## Installation

Clone the repo into your Claude Code skills directory so each skill becomes available as a slash command.

```bash
git clone git@github.com:zkwokleung/lingua-claude-skills.git ~/.claude/skills/lingua-claude-skills
```

Alternatively, symlink an individual skill into `~/.claude/skills/`:

```bash
ln -s "$PWD/japanese/jlpt-question" ~/.claude/skills/jlpt-question
```

Restart Claude Code (or start a new session) and the skill will be discoverable.

## Usage

Invoke a skill by its slash command. For example:

```
/jlpt-question N3
```

Claude will produce one question and wait for your answer. Reply with the option number (1–4); Claude grades it and offers another.

Each skill's `SKILL.md` documents its arguments and behavior in detail.

## Repository layout

```
.
├── japanese/
│   └── jlpt-question/
│       └── SKILL.md
└── README.md
```

Each skill lives in its own directory under a language folder and is defined by a `SKILL.md` file with YAML frontmatter (`name`, `description`) followed by the skill's instructions.

## Contributing

New skills are welcome. To add one:

1. Create a directory under the appropriate language folder (e.g. `japanese/my-skill/`). Add a new language folder if needed.
2. Add a `SKILL.md` with frontmatter:
   ```yaml
   ---
   name: my-skill
   description: One-line description of what the skill does and when to use it.
   ---
   ```
3. Write clear, step-by-step instructions for Claude. Keep the scope focused — one skill, one job.
4. Update the table in this README.

## License

See repository for license details.
