# Brunel bench

Open test cases and results for software bots and AI agents working inside business systems.

- `cases/`: 17 tasks on Odoo 17 and osTicket, each with database checks that prove the result
- `docs/method.md`: how runs are done and judged
- `docs/human-baseline.md`: how many actions a person needs for each task
- `results/2026-11-17/`: first results, two AI agents, 5 runs per task (`report.html` to read, `report.json` for the numbers)

First finding: the cheaper agent reported a project task as done 7 times when it was still open in the database.

Case format: https://github.com/Brunel001/cases-format · Contact: founder@brunelconsulting.com · https://brunelconsulting.com

Licensed under Apache 2.0.
