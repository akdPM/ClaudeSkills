---
name: design-reference-research
description: "Research real design references before designing or redesigning any screen, then turn them into concrete directions. Use this whenever the user asks for design references, inspiration, a moodboard, \"what do good ones look like\", a visual direction or theme, or is about to design or revamp a dashboard, CMS or builder screen, a landing page, a portfolio or case-study page, a mobile app screen, or a component such as a hero, pricing section, navbar, footer, empty state or onboarding flow. Also use it when the user says a design feels flat, generic, dead or \"not like a SaaS\", because the fix starts with looking at references. Use it even if the user does not say the word \"reference\"."
---

# Design reference research

Design work goes better when it starts from real, named examples instead of from memory. This skill finds those examples in the user's own curated list of sources, records exactly what is worth borrowing from each, and turns the findings into two or three directions the user can choose between.

The user keeps a list of 65 reference sites. It lives in `references/sources.md`, grouped by purpose. Read that file before searching so you look in the places the user already trusts.

If the work is for the user's portfolio-builder product (working name Project Delta), also read `references/project-delta.md`. It maps each part of the product to the sources and questions that matter for it.

## Ask before starting

The user wants to decide when this skill runs. When a design or redesign task comes up, do not start researching on your own. Ask one short question first, for example: "Shall I run the design-reference-research skill before I design this?" If other design skills are available, name them in the same question so the user can pick. Start only after a yes. If the user asked for this skill by name, that is the yes.

## The workflow

### 1. Pin down what is being designed

Write one line each for:

- **Surface:** builder or dashboard, marketing landing page, public portfolio or case study, mobile app, or a single component.
- **The screen's job:** what the person on it is trying to get done.
- **Audience:** who uses it and what they are comparing it to.
- **Feel wanted:** the user's own words, if they gave any ("alive", "calm", "premium", "not like a form").
- **Constraints:** existing brand, fonts, colours or components that must stay.

If the surface or the job is unclear, ask once. Do not ask about anything you can reasonably infer.

### 2. Choose where to look

Pick three to five sources from `references/sources.md` that fit the surface. Section galleries are for single components, flow libraries are for app screens, and award galleries are for landing pages and motion. Using the right kind of source matters more than using many.

### 3. Collect real references

Open the sources and find five to eight references per screen or component. For each one, record:

- **Name and link** to the actual page or shot.
- **What it is** in a few words.
- **What to borrow:** one specific, nameable thing, such as "sticky section index with reading progress" or "empty state that offers three templates". "Clean layout" is not specific enough to act on.
- **Why it fits** this screen's job.
- **What not to borrow**, if something in it would hurt here.

Only list references you have actually opened in this session. A reference you cannot show is worse than no reference, because the user will go looking for it. If a source cannot be reached (blocked, needs a login, or no browsing tool is available), say so plainly, name the sources you could not open, and offer two ways forward: the user pastes links or screenshots, or you describe well-known patterns and label them as coming from general knowledge, not from a page you opened.

Prefer shipped products over concept shots. Concept shots often ignore real content, empty states and small screens.

### 4. Find the patterns

Look across what you collected and write down what repeats: layout structure, how hierarchy is shown, type choices, colour use, density, motion, and how empty and loading states are handled. Three references doing the same thing is a pattern worth naming. One striking example is an option, not a pattern.

### 5. Propose directions

Turn the patterns into two or three directions that genuinely differ from each other. For each:

- **A short name** the user can refer to.
- **The idea** in one sentence.
- **Borrowed from:** the references behind it.
- **What it changes** on this screen, as a short list.
- **Trade-off:** what it costs or risks.

Say which one you would pick and why. Then stop and let the user choose before building anything.

### 6. Hand over

Use this structure for the write-up:

```
# References: <screen or component>

## What this screen has to do
## References
| Reference | What it is | Borrow | Why it fits |
## Patterns across them
## Directions
### 1. <name>
### 2. <name>
## Recommendation
## Could not open
```

Where it goes depends on the session:

- If a design canvas is in use, add a "References" page to it and put the findings beside the screens they inform.
- Otherwise write a document, or reply in chat if the user asked a quick question.

## Rules that keep the output useful

- **Borrow patterns, never copy a design.** Take the structure, the interaction or the idea. Do not reproduce another company's layout, artwork, illustrations or copy. This keeps the user's product original and out of legal trouble.
- **Fonts, illustrations and stock assets have licences.** When suggesting one from the sources, note whether it is free for commercial use or needs a licence, or say that you have not checked.
- **Check the borrowed idea against real content.** A layout that works with a short headline and one image may fail with the user's actual text. Say so when you see it.
- **Keep accessibility in the frame.** Flag references that depend on low-contrast text, tiny type or motion that cannot be turned off.
- **Match the amount of research to the ask.** One component needs five references and a few minutes. A whole visual direction for a product needs each surface covered.

## Other design skills

The user has other design skills installed in some environments (for example a research-first design skill, style and palette libraries, motion vocabulary, and design critique). If any are available in the session, use this skill to gather and organise references first, then hand the chosen direction to those skills for execution. If none are available, carry on with this skill alone.
