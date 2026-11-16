---
name: product-council
description: "Convene a council on a product decision or a piece of work: five thinkers (First Principles, Contrarian, Expansionist, Outsider, Executor) plus specialists for the stage, who answer separately, review each other anonymously, and produce one verdict. Use whenever the user says council, run the council, stress test, get more perspectives, or asks for a review of an MVP scope, wireframe, feasibility call, PRD, eval plan, pricing, go-to-market plan or analytics plan, and for any decision with real trade-offs. Not for factual lookups or small reversible choices."
---

# Product council

A council gives one decision or one piece of work several independent readings, then a single verdict. It exists because one voice, including the main assistant, anchors on its first idea.

## The panel

**Always seated: the five thinkers.** Each has its own skill with full instructions; read the ones you seat.

| Thinker | Asks |
|---|---|
| First Principles (`first-principles-thinker`) | What are we really solving, and what is the smallest thing that solves it? |
| Contrarian (`contrarian`) | What is wrong, missing, or going to fail? |
| Expansionist (`expansionist`) | What is the bigger opportunity? |
| Outsider (`outsider`) | Does this make sense to someone seeing it cold? |
| Executor (`executor`) | What do we do first, and what does it cost? |

**Added per stage: two or three specialists.** Read `references/stages.md` for who they are and what the verdict must contain at each stage. If the stage is unclear, ask which one applies.

For a quick question, seat three: First Principles, Contrarian, Executor. For an MVP, First Principles and Executor lead.

## The process

1. **Frame it.** Rewrite the question neutrally: what is being decided, the constraints, and what success looks like. Gather only the context the panel needs. Ask one clarifying question if the request is too vague to judge.
2. **Independent answers.** Each member answers alone, seeing only the framed question and its own role. Where separate agents are available, run each member as its own agent with no conversation history, because a shared history makes them agree. Where they are not, write each answer in turn without rereading the others, and say that the panel was simulated in one pass. Each answer: a position, the reasoning, the biggest risk, and what others may miss. 150 to 300 words, no hedging.
3. **Anonymous review.** Shuffle the answers and label them A, B, C and so on. Each member reads all of them without knowing who wrote which, and says: which is strongest and why, the biggest blind spot across them, and what every answer missed. Anonymity stops members deferring to a role.
4. **Verdict.** A chairman, who is not one of the members, reads everything and writes the verdict. The chairman may side with one dissenter over the majority when the reasoning is stronger, and must always report the strongest dissent even when rejecting it.

Do not force agreement. A real disagreement, clearly stated, is more useful than a blended answer.

## Output

```
## Council verdict: <topic>
**Stage and panel:**
**Where the council agrees:**
**Where it disagrees:** the positions, and who holds them
**Strongest dissent:** stated fairly, even if rejected
**Blind spots it caught:**
**Recommendation:**
**The one thing to do first:**
```

Show the verdict by default. Offer the individual answers and reviews, and show them if the user asks or has said they prefer to see them.

## Cost

A full council is many model calls. Say so before running a full panel on something small, and suggest the three-seat version.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the product-council skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
