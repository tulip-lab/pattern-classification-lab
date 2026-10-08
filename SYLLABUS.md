# Pattern Classification Practical Syllabus

## Purpose

The practical sequence turns the public common-core concepts into inspectable, reproducible classification workflows. Each reviewed practical should connect to one or more common-core outcomes and make its evidence requirements clear. The detailed topic-to-session relationship and known gaps are maintained in the [common-core and practical map](PRACTICAL-MAP.md).

## Practical learning pattern

1. identify the question, expected output, and prerequisites;
2. run or build a small baseline;
3. inspect intermediate data, parameters, predictions, or diagnostics;
4. test normal, edge or missing-information, and failure behaviour;
5. compare alternatives using appropriate evaluation evidence; and
6. restart and run from the top, record limitations, and reflect on transfer.

## Current status

Eight executable, student-facing practical candidates are present locally. M10 and M11 add curated paths to established public exercises in the Agentic AI and SIT742 Labs while preserving those exercises' source identities. Code and original narrative licences are recorded; publication remains subject to explicit approval.

| Session | Module | Practical | Primary outcomes | Status |
| --- | --- | --- | --- | --- |
| M02A | M02 Foundations | [Classification workflow and features](M02-Foundations/M02A-Classification-Workflow-and-Features.ipynb) | CLO1, CLO2 | Executable candidate |
| M03A | M03 Decision Theory | [Bayesian decision and decision boundaries](M03-Decision-Theory/M03A-Bayesian-Decision-and-Boundaries.ipynb) | CLO1, CLO3 | Executable candidate |
| M04A | M04 Parameter Estimation | [MLE, MAP, and EM](M04-Parameter-Estimation/M04A-Parameter-Estimation-MLE-MAP-EM.ipynb) | CLO2, CLO3 | Executable candidate |
| M05A | M05 Parametric Models | [HMM and Naive Bayes](M05-Parametric-Models/M05A-Probabilistic-Models-HMM-and-Naive-Bayes.ipynb) | CLO1, CLO2, CLO3 | Executable candidate |
| M06A | M06 Nonparametric Methods | [Parzen and KNN](M06-Nonparametric-Methods/M06A-Nonparametric-Classification-Parzen-and-KNN.ipynb) | CLO2, CLO3 | Executable candidate |
| M07A | M07 Stochastic Methods | [From simulation to decision](M07-Stochastic-Methods/M07A-Stochastic-Methods-from-Simulation-to-Decision.ipynb) | CLO2, CLO3 | Executable candidate |
| M08A | M08 Discriminant Functions | [Optimisation and SVM](M08-Discriminant-Functions/M08A-Discriminant-Functions-Optimisation-and-SVM.ipynb) | CLO3 | Executable candidate |
| M09A | M09 Model Evaluation | [Model selection and generalisation](M09-Model-Evaluation/M09A-Model-Selection-and-Generalisation.ipynb) | CLO4 | Executable candidate |

M01 orientation is defined in navigation. M10 uses selected Large Language Model and Agentic AI exercises from the Agentic AI Lab, and M11 uses the differential privacy path from the SIT742 Lab. M07A supplies the continuous simulation-to-decision practical; Monte Carlo tree search remains an optional conceptual extension in the lecture material. M05 also requires a later Bayesian-network practical, while M03 and M09 need deeper cost-sensitive decision and PAC-learning activities respectively.

## Cross-cutting requirements

- Use approved public or synthetic data and record provenance.
- Support Google Colab or another online environment where practical.
- Keep optional package, accelerator, or API-dependent work separate from the mandatory learning path.
- Never require a learner to expose a credential in notebook source or output.
- Include accessibility guidance for visualisations and non-text artefacts.
- Defer collaboration, acknowledgement, and AI-use rules to the approved offering layer; do not invent institution-specific policy in the common lab.
