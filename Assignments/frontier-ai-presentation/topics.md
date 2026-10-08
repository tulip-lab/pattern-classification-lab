# Task 1 candidate topic catalogue

## Structure

The catalogue contains five themes and ten candidate topics. Each theme has two equally eligible topics and connects named Pattern Classification modules to a current research problem. More than one group may select the same topic code when its dataset, method, baseline, or evaluation emphasis is different.

Each topic has at least one confirmed journal or conference starting reference. Several topics deliberately include a TULIP Lab publication so that students can connect the course to research produced by the teaching team. A starting reference frames the problem; it is not a method that students must reproduce in full.

## T01 — Quantum machine learning for classification

Quantum ML work must test a falsifiable classification claim against strong classical baselines. A local noiseless or shot-based simulator is sufficient; access to real quantum hardware is neither required nor rewarded. Students must not claim quantum advantage from one small dataset or favourable run.

### T01-A — Quantum kernel versus classical kernels

- **Question:** Does a quantum feature map produce a useful similarity measure for a small classification problem beyond linear and RBF kernels under the same split and preprocessing?
- **Course modules:** M02 probability and measurement; M06 kernel methods; M08 SVM decision boundaries; M09 validation and generalisation.
- **Frontier connection:** quantum feature maps, fidelity quantum kernels, hybrid quantum–classical classification, simulator-based QML benchmarking.
- **Minimum experiment:** use 2–6 leakage-safe transformed features/qubits and compare linear SVM, RBF SVM, and a fixed quantum-kernel SVM on the same held- out or cross-validation folds. Report macro-F1, balanced accuracy, kernel matrix diagnostics, runtime, circuit evaluations/shots, seed or shot sensitivity, and failed cases.
- **Starting reference:** Jerbi et al., [Shadows of quantum machine learning](https://www.nature.com/articles/s41467-024-49877-8), *Nature Communications*, 2024. Havlíček et al.'s 2019 quantum-feature-space paper is the foundational method reference.

### T01-B — Variational quantum classifier versus a matched classical model

- **Question:** Under a small fixed compute budget, how does a variational quantum classifier compare with logistic regression and a small MLP using the same transformed inputs?
- **Course modules:** M04 parameter estimation and optimisation; M08 discriminant functions; M09 model selection.
- **Frontier connection:** parameterised quantum circuits, hybrid quantum–classical optimisation, variational quantum classifiers, noise and shot sensitivity.
- **Minimum experiment:** compare majority, logistic-regression, small-MLP, and VQC baselines with fixed data folds, seeds, tuning budget, and stopping rule. Report macro-F1, balanced accuracy, optimisation curves, runtime, circuit depth/two-qubit gates, shots, seed variability, and representative failures.
- **Starting reference:** [Superior resilience to poisoning and amenability to unlearning in quantum machine learning](https://www.nature.com/articles/s41467-026-70420-4), *Nature Communications*, 2026. The official Qiskit VQC tutorial is implementation documentation rather than the required scholarly evidence.

## T02 — Privacy in quantum, LLM, and agentic AI

Privacy projects must measure both privacy risk and task utility. Attacks are restricted to public benchmarks, local sandbox systems, or synthetic records and secrets created for the experiment. Testing a live service, another person's account, or real confidential data is prohibited.

### T02-A — Quantum privacy preservation

- **Question:** Can a quantum or hybrid privacy mechanism reduce an explicitly defined leakage or distinguishability measure while retaining useful classification performance compared with non-private and classical-noise baselines?
- **Course modules:** M02 probability, noise, and information; M03 privacy– utility loss; M06 kernels; M09 evaluation; M11 privacy.
- **Frontier connection:** quantum differential privacy, noise-aware privacy, quantum kernel inducing points, privacy auditing of quantum models.
- **Minimum experiment:** on a small simulator-compatible dataset, compare a non-private classifier, a documented classical perturbation/DP baseline, and one quantum or hybrid privacy condition. Report privacy budget or a justified empirical leakage proxy, attack success where safe, macro-F1/balanced accuracy, calibration, runtime, shots/noise settings, and the privacy–utility curve. A literature-plus-reproduction study may implement a simplified mechanism but must state what theoretical guarantees it does not reproduce.
- **Starting references:** Song et al., [Toward a Hybrid Quantum Differential Privacy](https://arxiv.org/abs/2501.07844), *IEEE Journal on Selected Areas in Communications* 43(8), 2025; and Song et al., [Quantum-KIP: Kernel Inducing Points for Quantum Privacy](https://signalprocessingsociety.org/publications-resources/ieee-transactions-information-forensics-and-security/2026/09/quantum-kip), *IEEE Transactions on Information Forensics and Security*, 2026. Both are TULIP Lab publications.

### T02-B — Privacy attacks in the LLM and agentic-AI era

- **Question:** When an LLM or agent can read private context and act through tools, which conditions cause disclosure, and which safeguard best reduces leakage without destroying task utility?
- **Course modules:** M03 asymmetric privacy loss and abstention; M08 sensitive-content classification; M09 attack/defence evaluation; M10 LLM and agent decisions; M11 privacy and threat modelling.
- **Frontier connection:** training-data and membership leakage, inference-time contextual privacy, agent memory/tool leakage, prompt injection, privacy filters, least-privilege tool access.
- **Minimum experiment:** use PrivacyLens or an equivalent safe synthetic benchmark to compare an unprotected LLM/agent with at least two safeguards, such as privacy-aware prompting, PII filtering, access control, or action review. Report leakage/attack-success rate, privacy precision and recall, benign-task completion, false refusal, latency/cost, and failures by privacy category. Never insert real secrets or attack a live system.
- **Starting references:** Song et al., [Digital Privacy Under Attack: Challenges and Enablers](https://www.tulip.academy/publication/ps/), *ACM Computing Surveys*, 2025/2026, a TULIP Lab synthesis; and Shao et al., [PrivacyLens: Evaluating Privacy Norm Awareness of Language Models in Action](https://papers.nips.cc/paper_files/paper/2024/hash/a2a7e58309d5190082390ff10ff3b2b8-Abstract-Datasets_and_Benchmarks_Track.html), NeurIPS 2024 Datasets and Benchmarks.

## T03 — Counterfactual reasoning for classification and decisions

Counterfactual projects must distinguish a model counterfactual—an input change that alters a prediction—from a causal counterfactual about what would happen under an intervention. Causal language requires explicit structural and identification assumptions.

### T03-A — Counterfactual explanations and actionable recourse

- **Question:** Can a constrained counterfactual method find smaller, more plausible, actionable, and stable changes than a nearest-boundary or unconstrained baseline?
- **Course modules:** M03 actions and loss; M08 decision boundaries; M09 explanation evaluation.
- **Frontier connection:** counterfactual XAI, algorithmic recourse, generative/latent counterfactuals, structured decision pipelines.
- **Minimum experiment:** compare a nearest-boundary or simple perturbation baseline with one constrained or generative method on the same held-out cases. Report validity, proximity, sparsity, plausibility, actionability, diversity, stability, subgroup differences, and failed cases.
- **Starting reference:** Vivier-Ardisson et al., [CF-OPT: Counterfactual Explanations for Structured Prediction](https://proceedings.mlr.press/v235/vivier-ardisson24a.html), ICML 2024.

### T03-B — Causal counterfactual reasoning for targeted decisions

- **Question:** When does an explicitly causal counterfactual model recommend different actions from association-based feature importance or predictive recourse, and are those recommendations stable under plausible structural assumptions?
- **Course modules:** M02 conditional dependence; M03 decisions and interventions; M04 estimation; M09 validation and sensitivity analysis.
- **Frontier connection:** structural causal models, potential outcomes, counterfactual optimisation, targeted strategy design.
- **Minimum experiment:** use a synthetic structural causal model or an approved public dataset with defensible assumptions. Compare predictive feature importance/recourse with a causal counterfactual method; report action agreement, intervention cost, target-outcome change, sensitivity to graph or effect assumptions, subgroup effects, and cases where causal identification is not supported.
- **Starting reference:** Xia et al., [Destination Competitiveness Improvement: Insights From Causal Counterfactual AI Analysis](https://journals.sagepub.com/doi/10.1177/00472875251322512), *Journal of Travel Research*, online 2025 / volume 2026. This TULIP Lab paper extends the team's [AI-based counterfactual reasoning for tourism research](https://www.sciencedirect.com/science/article/pii/S0160738323000907), *Annals of Tourism Research*, 2023.

## T04 — Stochastic time-series and interval forecasting

This theme is a direct continuation of `M07`. Students must model a predictive distribution or generate stochastic forecast paths, not submit only a point forecast leaderboard. Temporal order must be preserved throughout training, calibration, model selection, and evaluation. Each project must also derive and evaluate at least one forecast-supported decision, such as a demand regime, risk state, anomaly/event, direction of change, or intervention trigger.

### T04-A — Gaussian-process time-series forecasting and posterior intervals

- **Question:** Under a rolling-origin evaluation, when do Gaussian-process forecasts provide more accurate and useful predictive intervals than a seasonal-naive and a classical statistical forecasting baseline?
- **Course modules:** M02 temporal dependence and probability; M04 Bayesian estimation; M06 kernels; M07 Gaussian processes and posterior prediction; M09 temporal evaluation and calibration.
- **Frontier connection:** scalable GP forecasting, stochastic-process kernels, non-stationarity, learned memory, and posterior predictive distributions.
- **Minimum experiment:** use at least one public time-series dataset and a rolling-origin protocol. Compare a seasonal-naive baseline, one classical model such as ETS or ARIMA, and a GP forecaster. Report MAE or MASE, 80% and 95% empirical coverage, mean interval width, weighted interval score, calibration by forecast horizon, runtime, and sensitivity to at least one kernel, context-window, or likelihood choice.
- **Starting reference:** Tóth et al., [Learning to Forget: Bayesian Time Series Forecasting using Recurrent Sparse Spectrum Signature Gaussian Processes](https://proceedings.mlr.press/v258/toth25b.html), AISTATS 2025. A simplified GP is acceptable; reproducing the full architecture is not required.

### T04-B — Stochastic predictive simulation and calibrated multi-horizon intervals

- **Question:** Do stochastic forecast paths, with or without post-hoc calibration, produce sharper multi-horizon prediction intervals at the required coverage than deterministic residual intervals or a bootstrap baseline?
- **Course modules:** M02 conditional distributions; M04 estimation; M05 stochastic state-space assumptions; M07 Monte Carlo reasoning and posterior prediction; M09 rolling-origin evaluation and interval calibration.
- **Frontier connection:** predictive simulation, stochastic differential or state-space models, generative forecasting, and conformal multi-horizon calibration.
- **Minimum experiment:** fit a feasible stochastic forecaster and generate at least 100 predictive paths per origin. Compare its uncalibrated sample quantile intervals with a simple residual or bootstrap interval and one calibrated variant. Report point accuracy, 80% and 95% marginal coverage, joint multi-horizon coverage, interval width, weighted interval score, seed/Monte Carlo variability, and failures during regime or variance change.
- **Starting references:** Chen et al., [Probabilistic Forecasting with Stochastic Interpolants and Föllmer Processes](https://proceedings.mlr.press/v235/chen24n.html), ICML 2024, for stochastic predictive ensembles; and Galvão Lopes et al., [ConForME: Multi-horizon Conditional Conformal Time Series Forecasting](https://proceedings.mlr.press/v230/galvao-lopes24a.html), COPA 2024, for interval calibration. A simpler stochastic state-space or Bayesian model may be used instead of reproducing the full ICML method.

## T05 — Learngene for efficient knowledge transfer

This theme extends the course's parameter-estimation, discriminant-function, and model-evaluation foundations to the Learngene programme pioneered by Xin Geng's group at Southeast University. Students study whether compact, task-agnostic model components can initialise descendant classifiers efficiently. “Learngene” is a machine-learning term here; projects about biological gene prediction are outside this topic.

### T05-A — Learngene initialisation for few-shot classification

- **Question:** Can a compact learngene inherited from an ancestry model help a descendant classifier learn novel classes with fewer labelled examples or fewer optimisation steps than random initialisation and ordinary transfer?
- **Course modules:** M04 parameter estimation and initialisation; M08 discriminant functions; M09 controlled comparison.
- **Frontier connection:** collective-to-individual learning, open-world classes, compact transferable knowledge, and data-efficient adaptation.
- **Minimum experiment:** use a small ancestry network or released checkpoint and a lightweight descendant classifier. Across at least three label budgets, compare random initialisation, ordinary full-model transfer or fine-tuning, and inherited compact layers or an explicitly identified learngene-inspired component. Report macro-F1 or balanced accuracy, convergence curves, repeated-seed variation, trainable/transferred parameters, time or compute, and at least one negative-transfer case. If the exact paper method is not implemented, label the method “learngene-inspired” and state the difference.
- **Starting references:** Wang et al., [Learngene: From Open-World to Your Learning Task](https://ojs.aaai.org/index.php/AAAI/article/view/20833), AAAI 2022, for the foundational classification formulation; and Xie et al., [KIND: Knowledge Integration and Diversion for Training Decomposable Models](https://proceedings.mlr.press/v267/xie25d.html), ICML 2025, for a current decomposable-model extension.

### T05-B — Adaptive Learngene pools for dynamic classification

- **Question:** Can a continually expanding pool of learngenes and a task-aware selector adapt descendant classifiers to new data distributions more efficiently than a fixed inherited component or ordinary full-model fine-tuning?
- **Course modules:** M04 sequential updating and parameter selection; M08 feature representations and classifiers; M09 ordered cross-task evaluation.
- **Frontier connection:** incremental knowledge accumulation, task-adaptive sparse selection, variable-sized descendant models, source-data-free reuse, and deployment under data or resource constraints.
- **Minimum experiment:** create an ordered sequence of at least three source tasks or partitions from which a small learngene pool can grow, followed by at least two downstream classification tasks or domains. Under matched label and optimisation budgets, compare random initialisation, ordinary transfer or fine-tuning, one fixed inherited component, and task-aware sparse selection from the pool. Report macro-F1 or balanced accuracy, average and worst-task performance, selection sparsity, transferred parameters and storage, retained source data, runtime, and negative transfer. A simplified selector is acceptable, but it must be labelled “adaptive-learngene-inspired” rather than an exact reproduction.
- **Starting reference:** Lin et al., [Adaptive-Learngene: Continual Expansion and Task-Aware Selection of Learngenes for Dynamic Environments](https://ojs.aaai.org/index.php/AAAI/article/view/39530), AAAI 2026.

## Common boundary

No topic receives credit merely for using a fashionable method, larger model, more agents, or more circuits. Every project must expose a course concept, a credible baseline, held-out or temporally ordered evaluation, controlled information/resource budgets, and an honest analysis of uncertainty and failure.

For `T01` and `T02-A`, novelty and circuit size do not earn credit by themselves. For `T02-B`, only safe sandbox or synthetic attacks are eligible. For `T03`, model recourse must not be presented as causal intervention without identification evidence. For `T04`, random train/test shuffling or fitting an interval calibrator on the final test window is leakage. For `T05`, students must distinguish an exact Learngene implementation from a learngene-inspired ablation. Credit comes from correct formulation, controlled comparison, reproducibility, and a conclusion proportionate to the evidence.
