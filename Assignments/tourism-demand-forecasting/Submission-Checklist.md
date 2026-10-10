# Assignment 2 submission checklist

Use this checklist before packaging the files required by the current offering.
The offering page remains authoritative for the deadline, delivery route, and
archive name.

## Data and temporal integrity

- [ ] The notebook loads and cites the approved public dataset.
- [ ] Training, validation, locked audit, and final periods match the brief.
- [ ] Random row splitting is not used.
- [ ] Preprocessing, feature selection, tuning, and calibration use no
  later-period information.
- [ ] Every external variable has a cutoff-safe availability date and licence.
- [ ] The locked public audit was opened only after the forecast protocol was
  frozen; any later work is clearly labelled exploratory.

## Forecast evidence

- [ ] Lag-1, lag-12, and at least one improved point method are compared.
- [ ] MAE, MASE, and MAPE are reported with explicit missing/zero handling.
- [ ] A simple interval baseline and at least one improved probabilistic method
  are compared.
- [ ] PICP, mean interval width, interval score/WIS, and coverage error are
  reported for both 80% and 95% intervals.
- [ ] Destination-level, horizon-level, baseline-difference, and failure
  evidence supports the final recommendation.

## CSV validation

- [ ] `Forecast.csv` contains exactly the required 12 months, `Date`, and the
  20 destination columns in template order.
- [ ] `Intervals.csv` contains exactly 240 rows and the required columns.
- [ ] All predictions are finite, numeric, and non-negative.
- [ ] Every interval satisfies
  `lower95 <= lower80 <= point <= upper80 <= upper95`.
- [ ] Point values agree between the two CSV files.
- [ ] `model_label` values are non-empty plain text without commas or line
  breaks.
- [ ] The supplied validator reports `PASS` for both files.

## Reproducibility and responsibility

- [ ] The notebook runs top to bottom in a clean environment and regenerates
  both CSV files without manual editing.
- [ ] The report stays within 15 main pages, excluding references and a concise
  reproducibility appendix.
- [ ] The forecast protocol, model card, and contribution declaration are
  complete and consistent with the notebook.
- [ ] Seeds, environment, compute, data provenance, external code, pretrained
  models, services, and AI/agent assistance are acknowledged and checked.
- [ ] No credentials, private links, personal/restricted data, hidden actuals,
  or instructor-only material appear in the package.
- [ ] Every group member reviewed the final package and contribution record.

## Required artefacts

- [ ] Notebook: `A2-Group-NAME-Notebook.ipynb`
- [ ] Report: `A2-Group-NAME-Report.pdf`
- [ ] Point forecasts: `A2-Group-NAME-Forecast.csv`
- [ ] Interval forecasts: `A2-Group-NAME-Intervals.csv`
- [ ] Frozen protocol: `A2-Group-NAME-Protocol.md`
- [ ] Model card: `A2-Group-NAME-Model-Card.md`
- [ ] Contribution declaration: `A2-Group-NAME-Contributions.md`
- [ ] Every `NAME` placeholder has been replaced by the assigned Group ID.
- [ ] All files open correctly and follow the current offering's packaging and
  submission instructions.
