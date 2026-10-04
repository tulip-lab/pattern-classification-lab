# Common-core and practical map

This map pairs the public common-core narrative with stable Lab session IDs.
It distinguishes material already present in this repository from legacy
references and curriculum gaps. A legacy link is not a canonical Lab
practical and must pass the review described in `AGENTS.md` before migration.

| Module | Common-core emphasis | Lab session or status | Evidence learners retain | Coverage note |
| --- | --- | --- | --- | --- |
| M01 | Course navigation, integrity, reproducibility, and safe data handling | Orientation only | Environment check and reproducibility checklist | Executable induction activity not yet required |
| M02 | Probability, features, modelling assumptions, and workflow | [M02A — Classification workflow and features](M02-Foundations/README.md) | Pipeline, cross-validation result, held-out result, and feature justification | Covers workflow application; mathematical derivations remain in the common core |
| M03 | Posterior decisions, loss, risk, and boundaries | [M03A — Bayesian decision and decision boundaries](M03-Decision-Theory/README.md) | Posterior calculations, boundary plot, and cost-sensitive comparison | Directly covers equal and asymmetric decision costs |
| M04 | MLE, MAP, latent variables, and EM | [M04A — MLE, MAP, and EM](M04-Parameter-Estimation/README.md) | Parameter comparison, responsibilities, convergence trace, and sensitivity result | Direct coverage |
| M05 | HMMs, Viterbi, and Bayesian networks | [M05A — HMM and Naive Bayes](M05-Parametric-Models/README.md) | Classifier evaluation and decoded state sequence | Bayesian-network practical remains a gap |
| M06 | Histograms, Parzen windows, and nearest neighbours | [M06A — Parzen and KNN](M06-Nonparametric-Methods/README.md) | Shared-protocol comparison and bias-variance interpretation | Histogram construction is supporting rather than the main task |
| M07 | Simulation, MCMC, diagnostics, Gaussian processes, temporal forecasting, and Bayesian optimisation | [M07A — From simulation to decision](M07-Stochastic-Methods/README.md) | MC estimate and MCSE, sampler diagnostics, GP forecast evidence, and acquisition history | Continuous greenhouse case; MCTS remains an optional conceptual extension |
| M08 | Discriminants, empirical objectives, margins, and kernels | [M08A — Optimisation and SVM](M08-Discriminant-Functions/README.md) | Loss trace, cross-validation results, and boundary explanation | Direct coverage of linear and kernel classifiers |
| M09 | Validation, metrics, comparison, and generalisation | [M09A — Model selection and generalisation](M09-Model-Evaluation/README.md) | Validation curves, learning curve, held-out result, uncertainty, and limitations | Cost-sensitive metrics and deeper PAC-learning remain extension work |
| M10 | Neural training, CNNs, and RNNs | [Coverage gap](M10-Deep-Learning/README.md) | Future baseline, training trace, held-out evaluation, and compute statement | No approved public practical yet |
| M11 | Privacy compromise and differential privacy | [Legacy candidates under review](M11-Privacy/README.md) | Future threat model, privacy parameters, utility comparison, and limitations | Dependency and rights review still required |

## Pairing principles

- The common-core module defines concepts and observable outcomes; the Lab
  session produces inspectable evidence of applying them.
- A practical need not reproduce every lecture topic. Gaps are recorded rather
  than hidden inside an overextended notebook.
- Model selection occurs without the final test set; held-out assessment is
  reported once the workflow is fixed.
- Practical evidence should include limitations, provenance, and responsible
  handling decisions where relevant.
- Collaboration and AI-use rules come from an approved offering, not this
  institution-neutral map.
