# Method

How every result in this repository is produced.

## Systems
Tasks run on disposable copies of open-source business systems: Odoo 17 (ERP) and osTicket (helpdesk), each loaded with the same demo data. Before every run the system is reset to that exact starting copy.

## Tasks
Each task is one file in `cases/`: a plain-language instruction, the screens the agent must not visit (settings, admin), a step and cost budget, and the database checks that prove the task was done. Every case is proven by hand before use: reset (checks fail), do it by hand (checks pass), reset again (checks fail).

## Runs
Each agent runs each task k times (k = 5 so far), from a fresh browser at 1280x800, starting logged in. Every action is recorded with the screenshot before it. Native dropdown lists are drawn inside the page so the agent can see them in screenshots.

## Verdict
A run passes only if the agent says it finished, did not visit a forbidden screen, and the database shows the correct result. A run where the agent said it finished but the database disagrees is counted as a false success.

## Numbers
- pass@1: share of all runs that passed.
- pass^k: share of tasks that passed in every one of their k runs.
- 95% range: Wilson interval on pass^k. With 17 tasks the ranges are wide; read them as early evidence, not final rankings.

## Human baseline
A person did every task by hand once and counted clicks, typing and key presses (waits not counted). See `docs/human-baseline.md`.

## Checking the judge
All 80 runs of the first batch were checked by hand against the automatic verdict: 80 of 80 agreed.

## Limits
Small task set, two systems, demo data, one person's baseline, costs estimated from token counts at list prices.
