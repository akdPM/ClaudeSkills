# Module PRD (detailed, one per module)

Use this when a product is large enough to split into modules. Each module gets its own document, built from this template. Product-level material (vision, sitemap, AI) lives in separate documents and is referenced, never copied.

## The document set

| Document | Written | Holds |
|---|---|---|
| Overview PRD | Once | Vision, verticals, who it is for, module list, how modules connect, success measures for the whole product |
| Sitemap | Once, updated as modules change | Every page and screen, grouped by area, with the module that owns it |
| Module PRDs | One per module | Everything about that module except AI behaviour |
| AI PRD | Once (`ai-prd.md`) | Every AI capability, by ID, plus the AI architecture and guardrails |
| Glossary | Once | Every product word (for example "Work", "Knowledge Base", "credit") in plain language |

## IDs (so everything can be referenced)

- Module code: two or three letters, for example `WK` (Work), `KB` (Knowledge Base), `PB` (Publishing), `RS` (Resume).
- Requirements: `WK-R01`. Screens: `WK-S01`. Flows: `WK-F01`. Edge cases: `WK-E01`. Events: `WK-A01` (analytics).
- AI capabilities: `AI-01`, defined only in the AI PRD.
- Screens also carry their design name, for example `WK-S03 · D8DocEditor`.

## Template

```
# <Module name> PRD
Module code · Owner · Date · Status · Version
Links: design canvas page · Overview PRD · Sitemap · AI PRD

## 1. In one paragraph
What this module lets people do, for whom, and why it matters. Plain words.

## 2. Problem and evidence
Who struggles, in what situation, what they do today, why that fails.
Real quotes with links. Mark anything that is a guess as "Assumption".

## 3. Goals, non-goals and how we measure success
- Goals: what changes for the person.
- Non-goals: what this module will not do, and why.
- Measures: the main number with a target, plus numbers that must not get worse.

## 4. Who uses it and when
Short stories: situation → what they do → what they get.

## 5. Where things come from (dependencies)
A table: what this module needs · which module or AI capability provides it · reference ID.
Example: "Confirmed facts · Knowledge Base · KB-R07" and "Case-study draft · AI · AI-04".
And the reverse: which other modules use this one.

## 6. Scope
Now / later / never, with one line of reasoning for anything debatable.

## 7. Screens
For each screen: ID and design name, an image or link, what it is for, what is on it, and where you can go from it.

## 8. User flows
One flow diagram per main journey (start, steps, decisions, ends), with the screen IDs on each step.
Then the steps written out in plain words.

## 9. Requirements
| ID | Requirement (plain words) | Why | Priority (must / should / later) | Acceptance criteria (Given / When / Then) | Screens | Uses |
Every "must" has acceptance criteria a tester can pass or fail.

## 10. States and edge cases
For every screen: empty, loading, success, error, partial, very long content, no permission, offline, first use, limits reached.
Then a numbered list of edge cases (WK-E01…) with what should happen.

## 11. Content and copy
Exact button labels, messages, errors and emails, so design and build use the same words.

## 12. Settings, permissions and limits
Who can do what; plan limits; credit cost per action (link to the AI PRD for the AI ones).

## 13. Data
What is stored, for how long, who can see it, how it is exported and deleted.

## 14. Analytics
Events (WK-A01…) with properties, and the question each one answers.

## 15. AI used by this module
A list of AI capability IDs with one line each and a link to the AI PRD. No AI detail here.

## 16. Accessibility and phone
Keyboard use, screen readers, contrast, behaviour at phone width.

## 17. Rollout
Stages, feature switch, what we watch, and when we roll back.

## 18. Risks
Each with likelihood, impact and what we do about it.

## 19. Open questions
Each with an owner and a date.

## 20. Decision log
What was decided, when and why.
```

## Rules

- Write for someone who has never seen the product. Plain words, short sentences, a term explained the first time it appears.
- Every requirement says why, so it survives scope cuts.
- Never describe the same thing in two places: reference it by ID.
- Keep screens in step with the design canvas. When a screen changes, update sections 7–11.
