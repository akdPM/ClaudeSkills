---
name: product-sense-check
description: "Judge whether a product idea or feature is the right problem, for the right person, solved in the simplest way, before anything is designed or specified. Use whenever the user asks whether something is worth building, wants a product-sense read, a problem statement, a sanity check on an idea, a product teardown or critique, or is about to start a PRD without a clear problem. Product sense applies at every stage, so also use it to re-check a plan mid-build or after launch data arrives."
---

# Product sense check

Product sense is making good product decisions when the situation is ambiguous. In practice it comes down to understanding the person well enough to find a need that matters, and being inventive enough to meet it simply. It is not a section of a PRD; it is the judgement applied before, during and after one.

## The check

Work through these in order and stop at the first that fails. A failed early question makes the later ones pointless.

1. **Who, exactly?** One specific person in one specific situation. "Product managers" is too wide; "a PM with three years' experience applying for senior roles who has no public work to show" is usable.
2. **What are they trying to get done, and what do they do today?** The current workaround is the real competitor.
3. **How much does it hurt, and how often?** Rare and mild problems do not support a product.
4. **Why would this solution win** over the workaround and over alternatives? Name the one thing it does clearly better.
5. **Is this the simplest thing that could work?** If a smaller version would test the idea, propose it.
6. **How would we know it worked?** One observable change in behaviour, and a number.
7. **For AI features:** does it need a model at all? What does a wrong answer cost the user, and would they notice? Is the quality the model can reach today good enough for this job?

## When there is evidence

If the user has interviews, support messages, analytics or reviews, read them before answering and quote what supports or contradicts each point. If there is none, say which answers are guesses and name the cheapest way to find out.

## Output

```
## Product sense: <idea>
**The person and the moment:**
**The job and today's workaround:**
**Why it matters:** pain and frequency
**Why this wins:**
**Simpler version worth trying first:**
**How we'd know:**
**AI check:** needed? cost of being wrong? good enough today?
**Verdict:** build, shrink, rethink or drop, with the reason
**Guesses to verify:**
```

Be willing to say drop. Offer the product council for a second opinion on anything close.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the product-sense-check skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
