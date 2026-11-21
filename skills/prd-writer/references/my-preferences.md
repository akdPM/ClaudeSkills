# The owner's PRD preferences

These override the templates wherever the two differ. Recorded 21 Nov 2026 from the owner's own instructions.

## Format
- **Detailed by default.** Use the short one-pager only when the owner asks for it.
- **One PRD per module.** A product is split into modules, for example Add Work, Work editor, Publishing, Site pages, Knowledge Base, Resume builder, Interview Studio, Billing and credits, Admin. Use `module-prd.md`.
- **Everything about a module lives in that module's PRD.** That covers its screens, flows, states, edge cases, settings, data, analytics, limits, pricing and permissions. A reader should never need another module's PRD to understand this one, except through the cross-references below.
- **AI is documented separately.** All model behaviour, prompts, evals, guardrails, fallbacks, cost and the AI architecture go in one AI PRD (`ai-prd.md`). Each module PRD lists the AI capabilities it uses by ID (for example `AI-04 Draft case study`) and links to them, and the AI PRD lists which modules use each capability. Nothing about AI is described twice.
- **Cross-references everywhere.** Every requirement, screen, flow and AI capability has an ID. Wherever one thing depends on another, say where it comes from, for example "Facts come from Knowledge Base, KB-R07" or "Uses AI-04". Add a "Where things come from" table to every module PRD.

## What every module PRD must contain
- The **screens**, embedded or linked from the design canvas by name, for example "D8PublishWork", so the PRD and the design stay in step.
- A **user flow diagram** for each main journey in the module.
- The **requirements table** with Given / When / Then acceptance criteria.
- **States and edge cases** for every screen.

## Product-level documents (written once, not per module)
- **Overview PRD:** vision, the verticals (portfolio, resume builder, interview platform, Career Ops), the module list and how modules connect.
- **Sitemap:** every page and screen, grouped by area, with links to the module PRD that owns it.
- **AI PRD:** see above.
- **Architecture notes:** services and integrations, written with engineering.

## Language
- **Write so anyone can understand it.** Use plain, everyday words and short sentences (under 20 words where possible). Explain a technical term the first time it appears, in brackets. Prefer "the page shows" to "the system renders". No buzzwords.
- Show examples instead of describing them: real button labels, real messages, real numbers.

## When designs change
When the owner changes a screen on the design canvas, update the PRD sections that reference it: the screen list, flows, requirements and states.
