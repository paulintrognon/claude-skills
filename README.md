# claude-skills

Personal [Claude Code](https://docs.claude.com/en/docs/claude-code) skills.

## Skills

| Skill | What it does |
|---|---|
| [`walkthrough`](skills/walkthrough/SKILL.md) | Walks you step by step through a complex topic, one concept at a time, until you can validate a decision, choose between options, or understand a problem. |

## Install

Copy a skill folder into `~/.claude/skills/`:

```bash
cp -r skills/walkthrough ~/.claude/skills/
```

Or link it, so a `git pull` updates it:

```bash
ln -s "$PWD/skills/walkthrough" ~/.claude/skills/walkthrough
```

## License

MIT
