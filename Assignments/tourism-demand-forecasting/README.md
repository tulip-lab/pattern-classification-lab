# Tourism demand forecasting project

Start with these materials:

1. [Specification](specification.md) — data, temporal protocol, required comparisons, output schemas, and reusable deliverables.
2. [Starter notebook](Tourism-Forecasting-Starter.ipynb) — a safe scaffold for loading the public data and producing the required files.
3. [Forecast template](templates/Forecast.csv) and [interval template](templates/Intervals.csv) — fill these without changing their rows or columns.
4. [Fictional forecast example](examples/Forecast.example.csv) and [fictional interval example](examples/Intervals.example.csv) — inspect these together to understand the required pairing and row structure; their values are invented and are not useful forecasts.
5. [Forecast protocol template](templates/Forecast-Protocol.md) — freeze the selection rules before opening the locked audit.
6. [Report outline](templates/Report-Outline.md) and [model card template](templates/Model-Card.md) — organise the evidence and describe the frozen final system.
7. [Contribution declaration](templates/Contribution-Declaration.md) and [submission checklist](Submission-Checklist.md) — complete these before packaging the assignment.
8. [Output validator](validate_submission.py) — checks structure and numeric constraints, but does not calculate marks or use hidden actuals.
9. Your current offering page — group rules, weight, dates, filenames, submission route, and applicable policy.

Quick validation command:

```bash
python validate_submission.py A2-Group-NAME-Forecast.csv A2-Group-NAME-Intervals.csv
```
