# Pattern Classification Lab

This public repository is the canonical home for student-facing practical
materials that accompany the
[Pattern Classification common core](https://github.com/tulip-lab/pattern-classification).

The repository is organised around stable `M01–M11` curriculum identities.
Eight executable practical candidates now cover M02–M09. They
use the repository's recorded code and teaching-content licences; publication
still requires an explicit commit and publication instruction. Legacy
practicals are provenance references rather than canonical copies.

## Start here

- [Practical syllabus and module status](SYLLABUS.md)
- [Common-core and practical pairing map](PRACTICAL-MAP.md)
- [Data policy](Data/README.md)
- [Assignment publication boundary](Assignments/README.md)
- [Assets policy](Assets/README.md)
- [Licensing status](LICENSING.md)
- [Licence and attribution notice](NOTICE.md)

## Modules

| Module | Practical area | Status |
| --- | --- | --- |
| M01 | [Induction](M01-Induction/README.md) | Orientation defined |
| M02 | [Mathematical Foundations](M02-Foundations/README.md) | M02A executable candidate |
| M03 | [Bayesian Decision Theory](M03-Decision-Theory/README.md) | M03A executable candidate |
| M04 | [Parameter Estimation](M04-Parameter-Estimation/README.md) | M04A executable candidate |
| M05 | [Parametric Models](M05-Parametric-Models/README.md) | M05A executable candidate |
| M06 | [Nonparametric Methods](M06-Nonparametric-Methods/README.md) | M06A executable candidate |
| M07 | [Stochastic Methods](M07-Stochastic-Methods/README.md) | M07A executable candidate |
| M08 | [Discriminant Functions](M08-Discriminant-Functions/README.md) | M08A executable candidate |
| M09 | [Model Evaluation](M09-Model-Evaluation/README.md) | M09A executable candidate |
| M10 | [Deep Learning](M10-Deep-Learning/README.md) | Alignment gap recorded |
| M11 | [Privacy](M11-Privacy/README.md) | Legacy candidates identified |

## Run locally

The guided paths use synthetic data or datasets bundled with scikit-learn and
do not require credentials or network downloads:

```bash
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
python -m pip install -r requirements.txt
jupyter lab
```

Each module page also provides a Google Colab link for its practical.

## Safety

Do not commit credentials, `.env` files, student submissions, grades,
identifiable feedback, unpublished solutions, private datasets, large model
weights, generated caches, or instructor-only material.
