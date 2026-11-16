---
name: product-analytics
description: "Plan what to measure in a product: the main metric, the supporting metrics, the events and properties to track, the funnels to watch, and for AI features the quality, cost and trust signals. Use whenever the user asks about analytics, metrics, KPIs, a north star, tracking plan, events, funnels, retention, activation, dashboards, Mixpanel, Amplitude or PostHog setup, or how to know whether a feature is working."
---

# Product analytics

Tracking is only useful if it answers a question someone will act on. Start from the questions, then define the smallest set of events that answers them.

## The method

1. **Write the questions first.** What do you need to know to decide what to build next? Five to ten questions.
2. **Choose the main metric.** One number that rises when users get real value, not when they merely show up. For a portfolio builder, "portfolios published and then viewed by someone else" says more than sign-ups.
3. **Add supporting metrics** along the journey: how people arrive, when they first get value, whether they come back, whether they pay, whether they tell others. Add one or two guardrail metrics that must not get worse.
4. **Define activation.** The specific action that predicts a user will stay, and the time allowed to reach it.
5. **Write the tracking plan.** One row per event: name, when it fires, properties, the question it answers. Keep to roughly five to fifteen key events at first.
6. **Name events consistently** before anything is built: lowercase with underscores, object then action, past tense, for example `project_published`. Inconsistent names are the most common reason analytics becomes unusable.
7. **Define the funnels** and the cohort view for retention.
8. **Decide the reviews:** what is looked at weekly, and what decision each view feeds.

## For AI features, also track

- **Use and completion:** started, finished, abandoned midway.
- **Acceptance:** output kept, edited (and how much), regenerated, or discarded. This is the best everyday quality signal.
- **Explicit feedback:** thumbs up or down, and reports.
- **Cost and speed:** tokens or credits per action, response time, failures and fallbacks.
- **Trust over time:** whether a user who had a bad result comes back.
Attach the model and prompt version to every AI event, so a change in quality can be traced to a change in the system.

## Two audiences

Separate analytics about how customers use the product from analytics the customer sees about their own visitors. They need different events and different privacy handling.

## Output

```
## Analytics plan: <product or feature>
**Questions to answer:**
**Main metric:** definition and why
**Supporting and guardrail metrics:**
**Activation:** the action and time window
**Tracking plan:** table of event, trigger, properties, question answered
**Funnels and retention view:**
**AI signals:**
**Review rhythm:**
**Privacy notes:** what is not collected, consent
```

Event naming here is a common practitioner convention, not a formal standard; match the user's existing scheme if they have one.

## Ask before starting

The user decides when this skill runs. When a task fits, ask one short question first ("Shall I use the product-analytics skill for this?") and start only after a yes. If the user named the skill, that is the yes.

## Who this is for

An indie AI product builder who is also an AI product manager. Assume small teams, limited budget, and products where a model produces part of the output. Wherever the work touches a model, cover quality, cost per use, latency and what happens when the model is wrong.
