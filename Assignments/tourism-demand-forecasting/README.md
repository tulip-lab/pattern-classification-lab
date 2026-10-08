# Tourism demand forecasting project

Start with these materials:

1. [Specification](specification.md) — data, temporal protocol, required comparisons, output schemas, and reusable deliverables.
2. [Starter notebook](Tourism-Forecasting-Starter.ipynb) — a safe scaffold for loading the public data and producing the required files.
3. [Forecast template](templates/Forecast.csv) and [interval template](templates/Intervals.csv) — fill these without changing their rows or columns.
4. [Model card template](templates/Model-Card.md) — briefly identifies the final system, reproduction requirements, intended use, and limitations.
5. [Output validator](validate_submission.py) — checks structure and numeric constraints, but does not calculate marks or use hidden actuals.
6. Your current offering page — group rules, weight, dates, filenames, submission route, and applicable policy.

Quick validation command:

```bash
python validate_submission.py Forecast.csv Intervals.csv
```
