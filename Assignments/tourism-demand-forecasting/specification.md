# Tourism demand forecasting project

## Goal

Build strong, reproducible point and interval forecasts for monthly Chinese outbound tourism demand. The data, temporal protocol, outputs, and evaluation measures are fixed; the forecasting algorithm is open.

Statistical, stochastic, machine-learning, deep-learning, foundation-model, quantum, hybrid, and ensemble methods are all permitted when justified. Novelty and complexity do not count as evidence of better forecasting.

## Dataset

Use the public TULIP Lab [ISF-TDF2023 dataset](https://github.com/tulip-lab/open-data/tree/main/ISF-TDF2023). It contains observations through `2023M07` and blank rows for the 12 forecast months. Blank target cells are not zero and must not be used as training data.

External data is optional. It must be public, licensed, reproducibly obtained, and historically available at the relevant prediction cutoff.

## Temporal protocol

| Stage | Target months | Permitted use |
| --- | --- | --- |
| Training | earliest valid month–`2022M07` | Fit preprocessing and candidate methods |
| Validation | `2022M08`–`2023M02` | Select method, features, hyperparameters, and interval construction |
| Locked public audit | `2023M03`–`2023M07` | Open once after freezing the workflow |
| Final forecast | `2023M08`–`2024M07` | Retrain through `2023M07` and generate final outputs |

Random row splitting is prohibited. Scaling, imputation, feature selection, calibration, and tuning must not use later-period information. Record the model-selection rule before opening the public audit; later experiments must be labelled exploratory.

## Required comparisons

For point forecasts, compare:

1. lag-1 naive;
2. lag-12 seasonal naive; and
3. at least one improved method selected from validation evidence.

For predictive intervals, compare a simple residual or seasonal-bootstrap baseline with at least one improved probabilistic method. Gaussian processes, Bayesian methods, quantile models, conformal methods, bootstrap approaches, probabilistic neural models, and other justified methods are eligible.

Report point accuracy using MAE, MASE, and MAPE, including results by destination and horizon. Report interval calibration and sharpness using PICP, interval width, interval score or WIS, and absolute coverage error. Discuss failures, stability, computation, and limitations.

## Required output: `Forecast.csv`

Start from [the template](templates/Forecast.csv). Keep exactly:

- one `Date` column;
- 12 rows from `2023M08` through `2024M07`;
- the 20 destination columns in their supplied order; and
- one finite, non-negative numeric forecast in every destination cell.

Valid numeric forms include `15342`, `15342.0`, and `15342.75`. Do not use thousands separators, percentage signs, formulas, `NaN`, `Inf`, blanks, notes, or extra columns.

## Required output: `Intervals.csv`

Start from [the template](templates/Intervals.csv). Keep its 240 rows and these columns exactly:

```text
Date,destination,point,lower80,upper80,lower95,upper95,model_label
```

For every row:

```text
lower95 <= lower80 <= point <= upper80 <= upper95
```

The `point` value must exactly match the corresponding value in `Forecast.csv`. All bounds must be finite numbers. `model_label` must be short, non-empty plain text without commas or line breaks.

Example:

```csv
2023M08,Canada,15342.75,14120.00,16580.00,13200.00,17450.00,my_model_v1
```

Run the supplied structural validator before finalising the package:

```bash
python validate_submission.py Forecast.csv Intervals.csv
```

Passing this validator confirms format only. It does not reveal hidden actuals or predict forecasting performance.

## Reusable deliverables

Prepare:

- a notebook that runs from top to bottom and generates both CSV files;
- a concise report explaining the protocol, baselines, selected method, evidence, failures, uncertainty, and conclusion;
- `Forecast.csv` and `Intervals.csv`; and
- sufficient provenance, AI/tool-use, environment, and contribution records to reproduce the work.

The current offering defines group size, weight, report limits, exact filenames, deadline, submission route, and institutional policy.

## Model card

Complete the supplied [model card template](templates/Model-Card.md) for the final system that generated `Forecast.csv` and `Intervals.csv`. The Protocol records the model-selection rules fixed before the locked audit; the Report presents the comparative evidence and conclusion; the Model Card gives a short factual record of the frozen final model, data cutoff, dependencies, resources, intended use, reproduction steps, and known limitations. It should point to the Report or Notebook rather than repeat their analysis.

## Optional frontier investigation

After the required baselines work, you may test one advanced stochastic or Gaussian-process idea using the same temporal protocol. Adopt it only when validation evidence supports better forecasting. Ideas explored in the frontier-AI presentation may be reused as methods, but reused code, literature, or configuration must be acknowledged.

## Responsible use

AI tools may support coding, debugging, search, and editing, or may form part of the forecasting method. Verify generated claims, citations, and code; record their purpose and relevant configuration. Do not expose credentials, personal data, restricted data, or hidden evaluation information.

The teaching team evaluates predictive performance, temporal validity, reproducibility, uncertainty, and the evidence supporting the final choice. The current offering supplies any formal rubric or mark allocation.
