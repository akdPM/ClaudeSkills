# Detailed PRD

Purpose: enough for design, engineering and testing to work without guessing. Include a section only when it has content; an empty heading adds nothing.

## Template

```
# <Feature or product name>
Owner · Contributors · Date · Status · Version · Links (designs, research, tickets)

## 1. Summary
Three or four sentences: the problem, the solution, the expected result.

## 2. Problem and evidence
The person and situation, what they do today, why that fails, and the evidence (research, data, quotes).

## 3. Goals, non-goals and success measures
- Goals: outcomes, not features.
- Non-goals: what this deliberately does not do, with reasons.
- Success measures: primary measure with baseline and target; guardrail measures that must not get worse; when they will be read.

## 4. Users and use cases
Who uses it, and the main scenarios as short stories: situation, action, result.

## 5. Scope
In this release / later / never. One line of reasoning for anything contentious.

## 6. User flow
The journey step by step, with entry points, decisions and exits. Link or embed the flow diagram and wireframes.

## 7. Requirements
A numbered table. Each row: ID, requirement, priority (must / should / later), acceptance criteria.
Write acceptance criteria so a tester can pass or fail them, for example:
"Given a published project, when the owner clicks Unpublish and confirms, then the public page returns not-found within 60 seconds."

## 8. States and edge cases
For each screen or action: empty, loading, success, error, partial, long content, no permission, offline, first use, and what happens at limits.
List the edge cases explicitly; this section is what separates a detailed PRD from a short one.

## 9. Design
Screens, components, copy, accessibility requirements, behaviour at phone width.

## 10. Data and analytics
What is stored, events to track with their properties, and the questions those events answer.

## 11. Technical notes
Constraints, dependencies, performance targets, security and privacy, migration. Written with engineering, not for them.

## 12. AI behaviour, evals and guardrails
Required when a model is involved. See ai-sections.md.

## 13. Pricing, limits and plans
Who gets it, on which plan, with what limits or credit cost.

## 14. Rollout
Stages (internal, beta, everyone), feature switch, what is watched, and the condition for rolling back.

## 15. Launch and communication
What is announced, to whom, where; help content; support readiness.

## 16. Risks
Each with likelihood, impact and mitigation.

## 17. Open questions
Each with an owner and a date.

## 18. Decision log
Decisions made, when, and why, so they are not reopened by accident.
```

## Rules

- Number requirements so they can be referred to.
- Every "must" has acceptance criteria.
- Keep the why near the what: a requirement with its reason survives scope pressure better.
- Update the document when decisions change; a stale PRD is worse than none.
