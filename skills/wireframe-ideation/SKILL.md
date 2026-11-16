---
name: wireframe-ideation
description: "Explore several layout and flow options for a screen or feature before any visual design, as low-fidelity wireframes with the reasoning for each. Use whenever the user asks for wireframes, layout options, a user flow, screen structure, how a page should be arranged, to sketch an idea, or is about to design or redesign a screen and has not yet settled its structure."
---

# Wireframe ideation

Structure first, looks later. Arguing about colour and type before the flow is settled is the most common way design work gets redone. This skill produces several structural options quickly so the user can choose with their eyes.

## The method

1. **State the job of the screen** in one sentence, and who is on it.
2. **Map the flow before any screen.** List the steps the person takes, the decisions they make and where they can go wrong. Mark the entry points and the exits.
3. **List what must be on the screen** as content and actions, in priority order, using real content where it exists. Placeholder text hides layout problems.
4. **Sketch at least three different structures**, not three versions of one. Vary the thing that matters: what is biggest, what comes first, one column or two, everything visible or revealed in steps, form or direct editing.
5. **Stay low fidelity.** Grey boxes, real labels, no colour, no icons beyond a marker. This keeps the conversation on structure.
6. **Cover the states** for the chosen option: empty, loading, error, long content, and phone width.
7. **Say what each option is good and bad at**, and recommend one.

## For AI features

Wireframe what a normal interface does not have: where the user gives input to the model, what they see while it works, how a draft is reviewed and accepted or rejected, how a wrong result is corrected, and where cost or credits are shown before an action.

## Output

- If a design canvas is in use, put each option on it as its own frame with a short note, side by side.
- Otherwise use simple text diagrams or a page.

```
## Wireframes: <screen>
**Job of the screen:**
**Flow:** numbered steps
**Must be on it:** in priority order
### Option A: <name>
What it is, the sketch, good at, weak at
### Option B / C
**Recommendation:**
**States still to design:**
```

Suggest `design-reference-research` first if no references have been gathered, and `product-council` at the design stage to choose between options.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the wireframe-ideation skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
