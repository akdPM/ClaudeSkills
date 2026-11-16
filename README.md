# ClaudeSkills

Personal skills for Claude, built around end-to-end AI product work: research, design, specs, evals and review.

A skill is a folder with a `SKILL.md` (when to use it and how) plus any reference files it needs. Claude reads the short description of every installed skill and loads the full instructions only when a task calls for one.

## Skills in this repo

| Skill | What it does | Status |
|---|---|---|
| [`design-reference-research`](skills/design-reference-research) | Before designing a screen, finds real references in a curated list of 65 sources, records what to borrow from each, and proposes two or three directions to choose from. | First version, not yet test-run |

## Working agreement

Claude asks before using any of these skills on a design or redesign task, and starts only after a yes. Naming a skill in the request counts as the yes.

## Installing a skill

**Claude apps (claude.ai, desktop):** zip the skill folder, rename the file to end in `.skill`, and upload it under Settings, Capabilities, Skills.

**Claude Code, for every project on your machine:**

```bash
cp -r skills/design-reference-research ~/.claude/skills/
```

**Claude Code, for one project only:** copy the folder into that project's `.claude/skills/` directory and commit it there.

## Layout

```
skills/
  <skill-name>/
    SKILL.md          instructions and trigger description
    references/       longer material loaded only when needed
```

## Adding a skill

1. Create `skills/<skill-name>/SKILL.md` with `name` and `description` in the front matter.
2. Keep `SKILL.md` short; move long lists and background into `references/`.
3. Add a row to the table above.
