# Sections an AI feature needs

Traditional templates assume software that behaves the same way every time. A model does not, so the PRD has to say what "good enough" means and what happens when the output is not. Manual checking cannot cover this; the evaluation plan is part of the requirement.

Add these to either format. In a short PRD, compress them into the "AI notes" block.

```
## AI behaviour

### What the model does
The task in plain words, its inputs (and where they come from), and its outputs (format, length, tone).

### Examples
At least five real input and output pairs: typical, difficult, and one that should be refused or flagged.

### Quality bar
What a good output is, as criteria a person could check. What is unacceptable (for example, stating facts not in the source).

### Evals
- Failure modes found from reading real outputs.
- For each: how it is tested, by code or by a judging model, as pass or fail.
- The test set: where the cases come from and how many.
- The threshold that must be met before release, and who signs off.
Write these with the eval-designer skill.

### Guardrails
- Input: what is rejected or cleaned before it reaches the model (injection attempts, personal data, off-topic use).
- Output: what is checked before the user sees it.
- Retrieval and tools: what the model may read and what actions it may take.

### When the model is wrong
What the user sees, how they correct or reject the result, and how the failure is recorded.

### Fallback
Behaviour when the model is slow, unavailable or over budget. How the feature is switched off without a release.

### Cost and latency
Expected cost of one use, cost at projected volume, the response-time target, and per-user limits or credit cost.

### Model and prompt ownership
Which model, who owns the prompt, how changes are tested before going live, and how prompts and evals are versioned as living requirements.

### Monitoring after launch
What is logged, what is reviewed and how often, and the signal that triggers a rollback.

### Data and privacy
What user data is sent to the model provider, what is stored, and what users are told.
```

Co-write the quality bar, evals and guardrails with whoever builds the AI part; a PM writing them alone tends to miss what is technically possible.
