---
name: technical-feasibility
description: "Assess whether and how a product idea or feature can be built: approach, build versus buy, risks, rough effort, and for AI features the quality, latency and cost per use. Use whenever the user asks if something is feasible or possible, how hard or expensive it would be, which approach or stack to use, whether to build or buy, how to de-risk a technical idea, or wants a spike or prototype planned."
---

# Technical feasibility

Feasibility is not yes or no. The useful answer is: here is the simplest approach, here is what could go wrong, here is what it costs, and here is the small test that would settle the open question.

## The assessment

1. **Restate what must be true** for the feature to work, as testable statements. "A case study draft comes back in under 60 seconds" is testable.
2. **Find the hard part.** Most of a feature is routine. Name the one or two parts that are uncertain and spend the effort there.
3. **Lay out two or three approaches** from simplest to most capable. Include buying or using an existing service. For each: what it needs, what it limits, effort, running cost.
4. **Check the constraints:** data available, privacy and security, dependence on outside services, scale, the skills on hand.
5. **Size it** in days of focused work and state what the estimate assumes.
6. **Plan the spike.** The smallest experiment that resolves the biggest unknown, with a time limit and a pass mark.

## For AI features, always answer

- **Does it need a model?** If rules or search would do, say so.
- **Quality:** can the model do the task well enough? Measure on real examples, not a demo. Reliability matters more than the best case.
- **Latency:** typical and worst-case response time, and whether the experience survives it.
- **Cost per use:** price of one action from input and output size, then at ten and a hundred times the volume. Input and output are priced differently.
- **Failure handling:** what the user sees when the model is wrong, slow or unavailable, and whether the feature can be switched off without a release.
- **Abuse:** what a hostile input does, and what limits exist per user.
- **Provider risk:** price changes, model retirement, outages. Keep the model behind one interface so it can be swapped.

State prices and limits as estimates and say where they came from; they change often and should be checked before a decision depends on them.

## Output

```
## Feasibility: <feature>
**What must be true:**
**The hard part:**
**Approaches:** table of approach, effort, running cost, limits
**Recommended approach:** and why
**AI check:** quality, latency, cost per use, failure handling
**Risks:** ranked, each with a mitigation
**Spike:** what to try, time limit, pass mark
**Verdict:** go, go with changes, spike first, or no
```

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the technical-feasibility skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
