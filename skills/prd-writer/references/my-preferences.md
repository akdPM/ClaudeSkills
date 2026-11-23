# The owner's PRD preferences

These override the templates wherever they differ. Last updated 21 Nov 2026 from the owner's own instructions.

## One PRD, not many
- **Write ONE PRD for the whole product.** Do not split it into an overview plus separate module documents. Use `module-prd.md` for the structure.
- **Inside it, describe features module by module.** Each module has its own part, and everything about that module lives there: what it is for, screens, user flows, requirements, states and edge cases, copy, settings, limits and data.
- **Group modules the way a user thinks about them.** For example, creating a Work and editing a Work are both part of the **Work** module, not two modules.
- **AI has its own part of the same PRD.** All model behaviour, prompts, evals, guardrails, fallbacks, cost and the AI architecture go in one "AI" part. Each module lists the AI capabilities it uses by ID (for example `AI-04 Draft a case study`) and links to them. Each AI capability lists the modules that use it. Nothing about AI is written twice.
- **Cross-reference everything.** Every requirement, screen, flow and AI capability has an ID. Wherever one thing depends on another, say where it comes from, for example "Facts come from the Knowledge Base (KB-R07)". Each module part has a short "Where things come from" table.

## What every module part must contain
- **Screens:** embedded or linked from the design canvas by board name (for example "D8PublishWork"), so the PRD and the design stay in step.
- **A user flow diagram** for each main journey.
- **Requirements** with Given / When / Then acceptance criteria.
- **States and edge cases** for every screen.

## Product-level parts (in the same PRD, before the modules)
- Vision and the product family.
- Problem and evidence.
- **Who it is for, defined properly:** personas backed by research, and full user stories per persona with acceptance criteria.
- **Research mapping:** customer research lives in its own document; the PRD links each decision to it.
- Goals and measures.
- **Sitemap**: every page, grouped the way users see them, with the module that owns each page. Draw it as a clear tree.
- Technical approach and architecture, written with engineering.
- Glossary, open questions, decision log.

## Language: a four-year-old should follow it
- Write so simply that a four-year-old could follow the idea. Use very short sentences (aim for 12 words or fewer), the most common everyday words, and one idea per sentence.
- No jargon. If a technical word is truly needed, explain it in plain words in brackets the first time.
- Say what a person sees and does: "You tap Publish. Your page goes live."
- Use real examples: real button labels, real messages, real numbers.

## Diagrams must be obvious at a glance
- One clear message per diagram, written as its title.
- Few boxes, plain names, arrows that follow the order people use things.
- If someone has to study it to understand it, simplify it or split it.

## Decisions the owner has made (follow them)
- Front end and back end are **separate**, in separate deployables, so a front-end failure never harms the back end.
- The marketing site and the app are separate: the marketing site at deltafolio.co, the app at app.deltafolio.co.

## Order of work
- Roadmap and designs come first. The technical PRD (architecture, AI agents and their harness) comes after the designs are final.
- Every Work step names where AI is used and what checks and balances apply.

## When designs change
When the owner changes a screen on the design canvas, update the PRD parts that reference it: screens, flows, requirements and states.
