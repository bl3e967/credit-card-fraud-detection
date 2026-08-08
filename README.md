# Credit Card Fraud Detection

An example data science project managed with the [Data Science Lifecycle
Process](https://github.com/dslp/dslp), where the issues are written and kept current by Claude
Code skills.

This is a **worked example, not a real project.** The scenario, the data and the results are
fictional — they follow the credit card fraud narrative from [the original DSLP
article](https://medium.com/data-science/dslp-the-data-science-project-management-framework-that-transformed-my-team-1b6727d009aa).
No model is trained here and no dataset is included. What's real is the issue structure and how
it got that way.

## Start with the Ask issue

**[#1](../../issues/1) is the point of the whole thing.** Read it top to bottom, then read its
comments.

The **body** is the high-level summary — problem, desired outcome, success criteria, constraints —
plus three sections that are maintained automatically: Datasets, Understanding and Exploration,
and Approaches and Experiments. Every child issue is summarised there, with the successful
experiment first and the failed one kept rather than deleted.

The **comment thread** is the audit trail, and it's where the project actually happened:

1. An action point list written after a corridor conversation, when almost nothing was known
2. Meeting notes that made it possible to fill in most of the body
3. An action point turning into the first Data issue
4. A design decision — restricting the training window — recorded with its reasoning and its cost
5. A status entry that surfaces what's still outstanding

That progression is the framework working. The Ask starts nearly empty and fills in as the project
teaches you what it is.

## The board

The [project board](https://github.com/users/bl3e967/projects/10) carries two single-select fields:

- **`Status`** — Ask, Data, Explore, Experiment, Model, Done. Group by this for the project view:
  what research is happening for this Ask.
- **`Progress`** — To Do, In Progress, Blocked, Waiting for Review. Group by this for a Kanban
  board that behaves the way everyone already expects.

Same items, two views. That's the two-board setup the original article argues for.

## The issues

| Issue | Type | Note |
| --- | --- | --- |
| [#1](../../issues/1) | Ask | The anchor. Everything links back here. |
| [#2](../../issues/2) | Data | One issue per *version* of a dataset. |
| [#3](../../issues/3) | Explore | Records what was **learned**, not what was run. |
| [#4](../../issues/4) | Experiment | Failed — and kept. |
| [#5](../../issues/5) | Experiment | Succeeded. Beat the baseline at fixed alert volume. |
| [#6](../../issues/6) | Experiment | On hold, blocked on compute. |

#4 is the one worth dwelling on: a failed approach, written down with its failure mode, so nobody
retries unsupervised anomaly detection on raw features in two years' time. Ordinary project
tracking throws that away.

## The sync markers

The Ask body contains marker pairs:

```markdown
<!-- dslp-sync:start experiment -->
<!-- dslp-sync:end experiment -->
```

`/dslp-sync` rewrites only what sits between a matching pair. The problem statement, success
criteria and constraints were written by a human and are never touched, and the comment thread is
never touched at all — that's what makes it safe to run automatically.

## The skills

The six skills that produced these issues are described in the accompanying article. They shell
out to `gh`, but nothing about DSLP depends on GitHub — the same templates and linking rules work
against Jira or Linear by swapping the CLI calls.

## Related

- [DSLP – The Data Science Project Management Framework that Transformed My Team](https://medium.com/data-science/dslp-the-data-science-project-management-framework-that-transformed-my-team-1b6727d009aa)
- [The Data Science Lifecycle Process](https://github.com/dslp/dslp)
