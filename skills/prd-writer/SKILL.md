---
name: prd-writer
description: "Write or review product requirements documents. Default for the owner: ONE detailed PRD for the whole product, with features described module by module, in language simple enough for a four-year-old, with screens, user flows and a sitemap, and all AI behaviour in its own part of the same PRD that modules reference by ID. Also writes a short one-page PRD or PR/FAQ on request. Use whenever the user asks for a PRD, spec, product brief, one-pager, requirements, feature write-up, PR/FAQ or pitch, wants an existing PRD reviewed or tightened, or needs an idea turned into something engineers can build from."
---

# PRD writer

A PRD exists so that everyone building something shares one understanding of the problem, what will be built, and how they will know it worked.

## Read first

**Always read `references/my-preferences.md` first.** It records how the owner wants PRDs written and overrides everything below where they differ. In short: one detailed PRD for the whole product, features described module by module, very simple language, screens and flows in every module, a sitemap, and AI in its own part with cross-references.

## Pick the format

| Format | Use it when | Read |
|---|---|---|
| **One full PRD, by module** (default) | A whole product, or anything handed over to build | `references/module-prd.md`, and `references/ai-prd.md` for the AI part |
| **Detailed PRD** | One self-contained feature | `references/detailed-prd.md` |
| **Short PRD or PR/FAQ** | Only when the owner asks for a quick one-pager | `references/short-prd.md` |

For a new product, write the one PRD in this order:
1. Product-level parts: vision, problem, goals, sitemap, technical approach.
2. Module parts, most important first.
3. The AI part, which grows as modules reference capabilities.
4. Glossary, open questions, decision log.

**If any part uses a model, the AI part is required, and `references/ai-sections.md` lists what each capability must cover.** An AI feature without evals is not specified, because nobody can say when it is good enough.

## How to write it

1. **Start from the problem, not the solution.** If the problem, the person and the evidence aren't clear, stop and run `product-sense-check` first, or ask.
2. **Gather before drafting.** Read the research, designs (design canvas boards), notes and earlier specs. Ask only for what is missing.
3. **Write so a four-year-old could follow it.** Very short sentences, the most common words, one idea per sentence, no jargon, real examples. Diagrams must be obvious at a glance.
4. **Give everything an ID and reference it.** Requirements, screens, flows, edge cases, events and AI capabilities each get an ID. Say where every input comes from.
5. **Show screens and flows.** Embed or link each screen by its design name. Draw a user flow for each main journey, and keep a product sitemap.
6. **Make requirements testable.** Use Given / When / Then. "Fast" is not a requirement; "the draft appears within 60 seconds for a 10-page upload" is.
7. **State what is out of scope**, with the reason.
8. **Mark every guess** as "Assumption" or "Open question" with an owner.

## Reviewing a PRD

Check, in this order:
1. Is the problem evidenced?
2. Is there one clear success measure?
3. Can every requirement be tested?
4. Are states and edge cases covered?
5. Is out-of-scope explicit?
6. Are screens and flows present and current with the design?
7. Do all cross-references resolve?
8. For AI: are evals, fallback and cost present in the AI part?
9. Is the language plain?

Report the gaps in priority order, then offer `product-council` at the PRD stage.

## Keeping it current

When designs or decisions change, update the PRD sections that reference them and add a line to the decision log. A stale PRD is worse than none.

## Personalising

When the owner shares PRD examples or corrects a PRD, record the difference in `references/my-preferences.md`.

## Ask before starting

The owner decides when this skill runs. When a task fits, ask one short question first ("Shall I use the prd-writer skill for this?") and start only after a yes. If the owner named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
