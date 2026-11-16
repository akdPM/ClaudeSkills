---
name: mvp-scoping
description: "Decide what goes into the first version of a product or feature and what is cut, by finding the riskiest assumption and the smallest thing that tests it. Use whenever the user asks to scope an MVP, plan a first version, cut scope, decide must-haves, prioritise features for launch, set a time budget, or says a project is growing too big."
---

# MVP scoping

A first version exists to learn whether the riskiest belief behind the product is true. Anything that does not help test that belief, or is not needed for a person to complete the core task, can wait.

## The method

1. **Write the bet.** "We believe [person] will [do what] because [why], and we will know when [observable result]."
2. **List the assumptions** behind the bet and sort them by two things: how damaging if wrong, and how little evidence there is. The one that is both damaging and unproven is the riskiest. Pick one, at most two.
3. **Set the appetite before the scope.** Decide how much time this is worth, for example two weeks or six, and fit the scope to it. Fixed time with flexible scope stops a first version growing without limit.
4. **Map the journey.** Lay out the steps a person takes from arriving to getting the result. Under each step list possible features.
5. **Draw the line.** For each feature ask: does it test the riskiest assumption, or is the journey impossible without it? If neither, it is below the line. Sort the rest as must, should, later.
6. **Fake what you can.** Anything that can be done by hand, bought, or stubbed for the first users should be, as long as users are not misled.
7. **Define done and the stop rule.** What result means continue, and what result means change course.

## For AI products

- The riskiest assumption is usually quality: can the model do this job well enough for this user? Test that with a prompt and twenty real examples before building any interface.
- Version one needs a way to see failures: log inputs and outputs, and give users a way to flag a bad result.
- Put a cost and a latency number on the core action before committing to it.

## Output

```
## MVP scope: <product or feature>
**The bet:**
**Riskiest assumption:** and how version one tests it
**Appetite:** time budget
**The journey:** steps
**In (must):**
**In if time (should):**
**Cut (later):** with what it costs to add later
**Faked or manual for now:**
**Done means / stop rule:**
```

Offer `product-council` at the MVP stage for a second read, with First Principles and Executor leading.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the mvp-scoping skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
