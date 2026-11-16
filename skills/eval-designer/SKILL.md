---
name: eval-designer
description: "Design evaluations for an AI feature: find the real failure modes, build a test set, write pass-or-fail checks, validate any judging model against human labels, and set the release bar. Use whenever the user asks for evals, how to test or measure an AI or LLM feature, a golden dataset, an LLM judge, a quality rubric, regression tests for prompts, what 'good' means for model output, or is writing a PRD for anything a model produces."
---

# Eval designer

An eval is a repeatable check that a model-powered feature does its job. The most common mistake is writing generic checks ("is it helpful?") before looking at real output. Good evals come from the failures you actually observe.

## The method

1. **Collect real outputs.** Use production traces if they exist. If not, write realistic inputs across the kinds of user and task you expect, run them, and keep the results. Aim for around a hundred.
2. **Read them yourself and take notes.** For each output write in plain words what is wrong, or that it is fine. Do this by hand for at least thirty before automating anything. This step, error analysis, is where most of the value is.
3. **Group the notes into failure modes** and count them. Stop when new outputs stop producing new kinds of failure. The counts tell you what to fix first.
4. **Write one check per failure mode.**
   - Prefer code where a rule can decide: format, length, required fields, forbidden content, a fact matching its source.
   - Use a judging model only for things that need judgement, such as tone or faithfulness. Give it one failure mode and a pass-or-fail answer. Avoid 1-to-5 scales; people cannot agree what separates a 3 from a 4, and a judge inherits that noise.
   - Expect four to seven judge-based checks for a typical product, not dozens.
5. **Validate each judge against people.** Label a set by hand, around fifty passes and fifty fails, and measure how often the judge catches real failures and how often it wrongly flags good output. Report both, not a single accuracy figure, because failures are usually rare.
6. **Build the test set.** Include typical cases, hard cases, cases that should be refused, and every bug found so far. Keep a portion aside that prompts are never tuned on.
7. **Set the bar.** State the pass rate needed to ship for each check, and which failures block release outright.
8. **Run them on every change** to a prompt, model or retrieval step, and keep reading samples of real output after launch. New failure modes appear with new users.

## What to cover beyond correctness

Faithfulness to source material, refusal of things it should not do, resistance to hostile input, consistency across repeated runs, response time, and cost per case.

## Output

```
## Eval plan: <feature>
**What the feature must do:**
**Failure modes observed:** table of mode, example, how often
**Checks:** table of failure mode, check type (code or judge), pass rule
**Judge validation:** catch rate and false-alarm rate against human labels
**Test set:** sources, size, held-out portion
**Release bar:** per check, and blocking failures
**When evals run / what is reviewed after launch:**
**Not yet covered:**
```

If no real outputs exist yet, say that the failure modes are predictions, and that the plan must be revised after the first real batch. The figures above are working guidance from practitioners, not fixed rules.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the eval-designer skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
