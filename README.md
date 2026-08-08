# Credit Card Fraud Detection

An example data science project managed with the [Data Science Lifecycle
Process](https://github.com/dslp/dslp), where every issue was written and is kept current by
Claude Code skills.

This is a **worked example, not a real project.** The scenario, the data and the results are
fictional — they follow the credit card fraud narrative from [the original DSLP
article](https://medium.com/data-science/dslp-the-data-science-project-management-framework-that-transformed-my-team-1b6727d009aa).
No model is trained here and no dataset is included. What's real is the issue structure.

## What to look at

**[The Ask issue (#1)](../../issues/1)** is the point of the whole thing. It's the single source
of truth for the project, and its Datasets, Exploration and Experiments sections are maintained
automatically — scroll to them and you'll see every child issue summarised, with the successful
experiment listed first and the failed one kept rather than deleted.

**[The board](https://github.com/users/bl3e967/projects/10)** carries the two fields DSLP asks
for: `Stage` (Ask/Data/Explore/Experiment/Model) and `Progress` (To Do/In Progress/Blocked/
Waiting for Review/Done). Grouping by one or the other gives you the two views the framework
depends on — the project board and the Kanban board.

**The issues themselves** show what each DSLP issue type is for:

| Issue | Type | Note |
| --- | --- | --- |
| [#1](../../issues/1) | Ask | The anchor. Everything links back here. |
| [#2](../../issues/2) | Data | One issue per *version* of a dataset. |
| [#3](../../issues/3) | Explore | Records what was **learned**, not what was run. |
| [#4](../../issues/4) | Experiment | Failed — and kept. This is the point. |
| [#5](../../issues/5) | Experiment | Succeeded. Beat the baseline at fixed alert volume. |
| [#6](../../issues/6) | Experiment | On hold, blocked on compute. |

#4 is the one worth dwelling on. A failed approach, written down with its failure mode, so nobody
on the team retries unsupervised anomaly detection on raw features in two years' time. Traditional
project tracking throws that away.

## The sync markers

The Ask issue body contains marker pairs:

```markdown
<!-- dslp-sync:start experiment -->
<!-- dslp-sync:end experiment -->
```

`/dslp-sync` rewrites only what sits between a matching pair. The problem statement, success
criteria and constraints in #1 were written by a human and are never touched by the agent — which
is what makes it safe to run automatically.

## The skills

The six skills that produced these issues are described in the accompanying article. They shell
out to `gh`, but nothing about DSLP depends on GitHub — the same templates and linking rules work
against Jira or Linear by swapping the CLI calls.

## Related

- [DSLP – The Data Science Project Management Framework that Transformed My Team](https://medium.com/data-science/dslp-the-data-science-project-management-framework-that-transformed-my-team-1b6727d009aa)
- [The Data Science Lifecycle Process](https://github.com/dslp/dslp)
