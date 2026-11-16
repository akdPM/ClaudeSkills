---
name: prd-writer
description: "Write or review a product requirements document in one of two formats: a short one-page PRD for quick alignment, or a detailed PRD covering every feature, state and edge case for hand-over. Includes the sections an AI feature needs: model behaviour, evals, guardrails, cost and fallback. Use whenever the user asks for a PRD, spec, product brief, one-pager, requirements, feature write-up, PR/FAQ or pitch, wants an existing PRD reviewed or tightened, or needs an idea turned into something engineers can build from."
---

# PRD writer

A PRD exists so that the people building something share one understanding of the problem, what will be built, and how they will know it worked. Its length should match the decision it supports.

## Pick the format

Ask which one the user wants if they have not said.

| Format | Use it when | Length | Read |
|---|---|---|---|
| **Short PRD** | Getting agreement to start, a small feature, an early idea, a first pass before a detailed one | One page | `references/short-prd.md` |
| **Detailed PRD** | Handing over to build, a complex feature, anything with many states or edge cases, work others will estimate and test from | As long as the feature needs | `references/detailed-prd.md` |

For a large initiative, write the short one first, get agreement, then expand it. A detailed PRD written before the problem is agreed is wasted.

**If any part of the feature uses a model, also read `references/ai-sections.md`.** An AI feature without evals in its PRD is not specified, because nobody can say when it is good enough.

## How to write it

1. **Start from the problem, not the solution.** If the problem, the person and the evidence are not clear, stop and run `product-sense-check` first, or ask.
2. **Gather before drafting.** Read whatever the user has: notes, research, designs, earlier specs. Ask only for what is missing and cannot be inferred.
3. **Write requirements someone can test.** "Fast" is not a requirement. "Draft appears within 60 seconds for a 10-page upload" is.
4. **State what is out of scope**, with the reason. This prevents more arguments than any other section.
5. **Mark every guess.** Label assumptions and open questions plainly so nobody builds on them unknowingly.
6. **Use real examples** of inputs, outputs and screens wherever possible.

## Reviewing a PRD

When asked to review, check: is the problem evidenced; is there one clear success measure; can each requirement be tested; are states and edge cases covered; is out-of-scope explicit; for AI, are evals, fallback and cost present. Report gaps in priority order, then offer `product-council` at the PRD stage.

## Personalising

The user will supply their own PRD examples and preferences. When they do, follow their structure and wording over the templates here, and note the differences in `references/my-preferences.md` so later PRDs match.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the prd-writer skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
