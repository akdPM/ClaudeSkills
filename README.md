# ClaudeSkills

Personal skills for Claude, built around end-to-end AI product work: research, design, specs, evals and review.

A skill is a folder with a `SKILL.md` (when to use it and how) plus any reference files it needs. Claude reads the short description of every installed skill and loads the full instructions only when a task calls for one.

## Skills in this repo

Sixteen skills covering the product cycle. All are first versions and have not been test-run yet. Each one asks before it runs.

### The five thinkers

Standing points of view, usable alone or seated on the council.

| Skill | The question it asks |
|---|---|
| [`first-principles-thinker`](skills/first-principles-thinker) | What are we really solving, and what is the smallest thing that solves it? |
| [`contrarian`](skills/contrarian) | What is wrong, missing, or going to fail? |
| [`expansionist`](skills/expansionist) | What is the bigger opportunity? |
| [`outsider`](skills/outsider) | Does this make sense to someone seeing it cold? |
| [`executor`](skills/executor) | What do we do first, and what does it cost? |

### The council

| Skill | What it does |
|---|---|
| [`product-council`](skills/product-council) | Seats the five thinkers plus specialists for the stage. They answer separately, review each other anonymously, and a chairman writes one verdict with the strongest dissent. |

### Stage skills

These produce the work; the council reviews it.

| Stage | Skill | What it does |
|---|---|---|
| Problem | [`product-sense-check`](skills/product-sense-check) | Is this the right problem, for the right person, solved simply? |
| Scope | [`mvp-scoping`](skills/mvp-scoping) | Riskiest assumption, time budget, what is in and what is cut |
| Design research | [`design-reference-research`](skills/design-reference-research) | Real references from 65 curated sources, turned into directions |
| Wireframes | [`wireframe-ideation`](skills/wireframe-ideation) | Flow first, then three or more low-fidelity structures |
| Feasibility | [`technical-feasibility`](skills/technical-feasibility) | Approach, build or buy, risks, effort; quality, latency and cost for AI |
| Specification | [`prd-writer`](skills/prd-writer) | Short one-page PRD or detailed PRD, with the sections AI features need |
| Evals | [`eval-designer`](skills/eval-designer) | Failure modes, test set, pass-or-fail checks, release bar |
| Pricing | [`pricing-and-credits`](skills/pricing-and-credits) | Cost per action, credit values, plans, margin |
| Launch | [`go-to-market`](skills/go-to-market) | Who it is for, positioning, message, channels, first hundred users |
| Measurement | [`product-analytics`](skills/product-analytics) | Main metric, tracking plan, funnels, AI quality signals |

### How they fit together

```
product-sense-check -> mvp-scoping -> design-reference-research -> wireframe-ideation
        -> technical-feasibility -> prd-writer + eval-designer
        -> pricing-and-credits -> go-to-market -> product-analytics

product-council can review the output of any stage.
```

### Personalising

`prd-writer` keeps a `references/my-preferences.md` file for your own PRD structure and wording. It is empty until you supply examples.

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
