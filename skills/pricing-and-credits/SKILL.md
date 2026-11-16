---
name: pricing-and-credits
description: "Design pricing for an AI product, especially credit-based plans: cost per action, credit values, plan tiers, margin and protection against heavy users. Use whenever the user asks about pricing, plans, credits, tokens, tokenomics, margins, unit economics, free tiers, top-ups, usage limits, or what an AI feature costs to run and what to charge for it."
---

# Pricing and credits

AI products have a cost for every use, so pricing has to start from what one action costs you. Typical software margins do not apply: AI products commonly target around 50 to 60 percent gross margin where ordinary software targets 70 to 80.

## The method

1. **List the actions that cost money.** Each model call, image, transcription or search the user can trigger.
2. **Work out the cost of each** from input size, output size and the model's price. Note the model tier used. Measure from real usage when available; label estimates as estimates.
3. **Add fixed costs:** hosting, database, tools, domains. Convert to a monthly figure.
4. **Model the users.** A typical user, a light one and a heavy one, with how many of each action they take in a month. The heavy user is the one who breaks plans.
5. **Set the credit.** Pick a simple value, for example 1 credit equals 1 cent of price, and price each action so that cost is at most about 40 percent of what the credits are worth. Round to numbers people can remember.
6. **Shape the plans.** The usual structure is a free allowance, one or two paid plans that include monthly credits, and top-ups. Decide what is free of credits entirely (anything with no marginal cost).
7. **Protect the margin.** Caps per user, rate limits, cheaper models for routine actions, and a visible cost before an expensive action.
8. **Check break-even.** Paying users needed to cover fixed costs at typical usage, and the margin if a user spends every credit.

## Decisions to make explicit

- Do unused monthly credits carry over? Do bought credits expire?
- What happens at zero: block, slow down, or offer a top-up?
- Is the free allowance one-off or monthly? A free tier is a cost, so cap it and require sign-in before any model call.
- Are prices shown before the action runs? They should be.

## Output

```
## Pricing: <product>
**Costly actions:** table of action, model tier, estimated cost
**Fixed monthly costs:**
**User models:** light / typical / heavy, with monthly cost to serve
**Credit value and price per action:** table with margin
**Plans:** free, paid, top-ups
**Safeguards:**
**Break-even:** paying users needed; margin at full credit use
**Assumptions to verify:**
```

Model and tool prices change often and public trackers disagree. Check current provider pricing before a decision depends on a number, and say where each figure came from.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the pricing-and-credits skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
