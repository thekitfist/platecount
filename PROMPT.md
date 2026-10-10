# LLM Prompt Used for Requirements Elicitation

**Model:** Claude Opus 5.5 (Anthropic)
**Date:** October 2026

## Prompt

> You are acting as a business analyst running the first pass of requirements elicitation for a new software product.
>
> **Product idea:** A meal planning and headcount system for Greek-life house kitchens, aimed at reducing food waste. I've worked in a sorority house kitchen twice a week for over a year, and the biggest recurring problem is that the kitchen rarely knows how many people will show up to a meal. Members sign out of meals inconsistently or not at all, so the staff either overcooks and throws food away or undercooks and runs out. Ordering suffers from the same guesswork, which wastes chapter money.
>
> The app should include:
> - A simple mobile sign-in/sign-out for each meal, with reminders and a cutoff time
> - A live headcount dashboard for kitchen staff
> - Late-plate requests handled in the app instead of by text
> - Dietary restriction and allergy flags attached to each headcount
> - Historical attendance data used to forecast turnout by day, meal and time of semester (exam weeks, game days, breaks)
>
> The scope should be achievable in one academic term: authentication, a small relational database, a mobile-friendly front end, and a basic forecasting feature that starts as simple averages.
>
> **Produce a product backlog** that represents the outcome of an initial elicitation pass. Requirements:
> 1. Identify the stakeholders and group requirements into epics.
> 2. Write functional requirements as user stories ("As a ___, I want ___ so that ___") and include non-functional requirements (security, privacy, performance, usability, reliability, accessibility).
> 3. Tag every requirement with metadata: unique ID, epic, type (functional / non-functional), primary stakeholder, MoSCoW priority, story point estimate (Fibonacci), and cross-cutting tags.
> 4. Identify dependencies between requirements, listing both what each requirement depends on and what it blocks, and show them as a dependency graph.
> 5. Give each requirement 1–3 testable acceptance criteria.
> 6. Mark features that are out of scope for this term as "Won't (this term)" rather than dropping them.
> 7. End with open questions that should be taken back to stakeholders in the next elicitation round.
>
> Output the backlog as Markdown, CSV and JSON.

## Review notes

- Checked that every dependency references a requirement that exists and that the graph has no cycles.
- Confirmed the critical path for an MVP (accounts → chapter setup → meal schedule → sign-in/out → cutoff → live headcount → stored actuals → forecast).
- Kept dietary and allergy data restricted to kitchen staff and the house director (REQ-028, NFR-004), since it is health information.
- Moved ingredient ordering and food cost tracking to "Won't (this term)" to keep the term scope realistic.
