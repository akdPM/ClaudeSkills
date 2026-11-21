# The AI part of the PRD

This is a part of the one PRD, not a separate document. Every AI capability is defined here once and given an ID. Module parts refer to these IDs and never repeat the detail. Read `ai-sections.md` for what each capability must cover.

## Template

```
## E. AI
Links: module parts · eval reports

## 1. In one paragraph
What AI does in this product, what it must never do, and the promise we make to users (for example "nothing invented; every claim has a source").

## 2. Capability index
| ID | Capability | Used by (module IDs) | Model tier | Credit cost | Status |
Example: AI-04 · Draft a case study · WK, KB · large · 10 · building

## 3. Architecture
- How a request flows: app → AI gateway → model → checks → user. Draw it.
- The AI gateway: routing between models and providers, fallbacks, retries, caching, cost tracking per user.
- Retrieval: how facts are found in the Knowledge Base and cited.
- Prompt registry: where prompts live, how they are versioned and tested.
- Evals and monitoring: tools, dashboards, alerts.
- Data and privacy: what is sent to providers, retention, region, user consent, training opt-in.

## 4. Shared guardrails (apply to every capability)
Input checks (prompt injection in uploaded documents, personal or confidential data), output checks (claims must match sources, banned content), tool and data access limits, rate and spend limits.

## 5. Model choice
For each tier: the model, why it was chosen (quality, speed, cost), the fallback, and when we re-evaluate.

## 6. Capabilities
One section per capability, each with everything in ai-sections.md:
what it does · inputs and outputs · examples · quality bar · evals · guardrails · when it is wrong · fallback · cost and speed · monitoring · data.
Each starts with "Used by:" and links back to the module requirements that call it.

## 7. Cost model
Cost per action, credits per action, margin, and limits per plan.

## 8. Risks, open questions, decision log
```

## Rules

- Plain language, as everywhere else.
- A capability used by several modules is written once here.
- Every capability has evals and a release threshold before it ships.
