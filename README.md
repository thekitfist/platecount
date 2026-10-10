# PlateCount

**A meal headcount and planning system for Greek-life house kitchens, built to cut food waste.**

## The problem

House kitchens rarely know how many people will show up to a meal. Members sign out inconsistently or not at all, so staff either overcook and throw food away or undercook and run out. Late plates are requested by text, dietary restrictions live in someone's head, and grocery ordering is guesswork, which wastes chapter money.

## The solution

PlateCount gives every member a two-tap sign-in/sign-out for each meal with a hard cutoff, gives kitchen staff a live headcount (with dietary and allergy breakdowns and a late plate list), and uses historical attendance to forecast turnout by day, meal and time of semester (exam weeks, game days, breaks).

## What's in this repository

This repository holds the output of the **first pass of requirements elicitation**: an initial product backlog generated with a large language model and reviewed for consistency.

| File | Contents |
|---|---|
| [`backlog.md`](backlog.md) | Human-readable backlog: metadata key, summary, epics, at-a-glance table, dependency graph, full requirement details with acceptance criteria, and open questions |
| [`backlog.csv`](backlog.csv) | Same backlog as a spreadsheet, importable into Jira, Azure DevOps, Trello or GitHub Projects |
| [`backlog.json`](backlog.json) | Same backlog in machine-readable form |
| [`PROMPT.md`](PROMPT.md) | The prompt given to the LLM and notes on how the output was reviewed |

## Backlog at a glance

- **48 requirements** (39 functional, 9 non-functional) across **9 epics** plus a non-functional group
- **MoSCoW priority:** 22 Must · 17 Should · 7 Could · 2 Won't (this term)
- **152 story points** total, 66 of them Must-haves
- Every requirement is tagged with epic, type, stakeholder, priority, estimate, cross-cutting tags, dependencies (`depends_on` and `blocks`) and acceptance criteria
- A Mermaid dependency graph in `backlog.md` renders directly on GitHub

### Epics

| Epic | Area |
|---|---|
| E1 | Accounts, Roles & Chapter Setup |
| E2 | Meal Schedule |
| E3 | Meal Attendance (Sign-in / Sign-out) |
| E4 | Late Plates |
| E5 | Dietary Restrictions & Allergies |
| E6 | Kitchen Headcount Dashboard |
| E7 | Notifications |
| E8 | Attendance Data & Forecasting |
| E9 | Ordering & Cost (Future) |
| NFR | Non-Functional Requirements |

## Stakeholders

Member · Kitchen Staff · House Director · Chapter Admin · Chapter Treasurer

## Process

The team will work in **Scrum** with two-week sprints. This backlog is the starting point for the first sprint planning session; priorities, estimates and open questions will be refined with stakeholders before items are committed to a sprint.
