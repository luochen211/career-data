# AGENTS.md — career-data

A public, append-only record of one person's career and income, plus the method anyone can copy. Everything committed here is visible to the world. Act accordingly.

## What goes where

| Kind of information | File | Rule |
|---------------------|------|------|
| Dated events (raise, offer, key conversation, project shipped, decision made) | `career-log.md` | Append only, newest at the bottom. Never rewrite an old entry; add a correction entry instead. |
| Income | `income/<year>.md` | One row per month: total as a multiple of the baseline, plus the share of each source. No absolute amounts in this public repo. Never round to look better. |
| One job | `employment/<company>.md` | Responsibilities, outcomes, compensation, how it felt. Update in place; log the change in `career-log.md`. |
| One long-running decision | `decisions/<yyyy-mm>-<slug>.md` | Premise, options, choice and reasoning, expected outcome with review dates, reviews appended. Never delete original reasoning. |
| Monthly review | `modes/review.md` defines the questions; answers go into `income/` and the relevant decision file | Run once a month. |

## Log entry format

```
## 2026-10-21 — <one-line event>
- 事实：what happened, in one or two sentences
- 来源：where this is known from (conversation, email, contract, commit)
- 影响：which file this changes, or "无"
```

## Hard rules

1. Never invent or round numbers. Unknown means `待确认`.
2. Keep facts and feelings separate: facts in `income/` and the tables of `employment/`, feelings in `career-log.md` or the `感受` section.
3. This repository is public. Never write the employer's name, absolute salary or income amounts, unannounced plans, other people's names, phone numbers, emails, private repository names, or anything learned under confidentiality. Refer to companies by industry and people by role. Those facts live in the owner's private repository.
4. Job-search operations (CV, trackers, evaluation reports, tailored CVs, recruiter contacts) do not belong here. They stay in a private career-ops data root.
5. Commit after each session of changes with a Conventional Commit message and push.
