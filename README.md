# Theo (Xiaotian) Yao

**Machine Learning · Software Engineering · AI**

I explore how neural networks learn and build reproducible software to evaluate them.
Currently seeking MLE, SDE, and AI engineering roles.

[LinkedIn](https://www.linkedin.com/in/xiaotian-yao/) · [LOTUS demo (access required)](https://github.com/elvisxtyao/LOTUS/blob/master/docs/project_showcase.md) · [Hebbian learning demo](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/project_demo.ipynb)

## Selected work

### [LOTUS — From single-cell research to model delivery](https://github.com/elvisxtyao/LOTUS)

*Private repository: project, evidence, and demo links below require access.*

How can we model changing cell states when lineage labels are incomplete?
LOTUS combines **identity/state representations and identity-locked dynamics**
with an auditable path from data preparation to evaluation and CPU inference.

**My engineering contribution**

| Research workflow | Model delivery and operations |
| :--- | :--- |
| Built disjoint cell splits, train-fitted preprocessing, resumable PyTorch training, MLflow tracking, and a sealed **seven-method, three-seed** evaluation. | Packaged fitted preprocessing and models for matching offline/CLI/FastAPI inference; verified installed-wheel Docker serving with real inputs. |
| Preserved baselines, per-seed results, and numerical/gradient checks in CI. | Verified frozen-artifact DVC recovery and local OCI/MLflow release rollback; separately exercised private AWS operations with a synthetic model. |

**Measured results.** In the fixed-budget LARRY H1 test (Day 4→6, held-out cells
within 206 seen clones, 512 features), **MLP led at 8.5182 ± 0.0494** versus
**9.7109 ± 0.1301 for no-growth**. These are clone-macro endpoint distances
(lower is better), mean ± sample SD across three training seeds on one split.
The no-growth engineering demo completed **2,718 requests with zero errors in
five minutes** locally: CPU, batch 1/4, concurrency 1, p95 **116.67/132.46 ms**.
This is a bounded serving check; real-model cloud serving and production SLOs
remain unverified.

**Verified stack →** [Python/PyTorch · pytest](https://github.com/elvisxtyao/LOTUS/blob/master/docs/training_integration_evidence.md)
· [GitHub Actions](https://github.com/elvisxtyao/LOTUS/blob/master/.github/workflows/ci.yml)
· [FastAPI · Docker](https://github.com/elvisxtyao/LOTUS/blob/master/docs/t08_model_card.md)
· [DVC](https://github.com/elvisxtyao/LOTUS/blob/master/docs/t15_real_dvc.md)
· [MLflow · OCI releases](https://github.com/elvisxtyao/LOTUS/blob/master/docs/t17_real_releases.md)
· [AWS EC2/SSM · Prometheus/Grafana (synthetic workload)](https://github.com/elvisxtyao/LOTUS/blob/master/docs/cloud_cpu_deployment.md)

**Explore →** [Three-minute walkthrough](https://github.com/elvisxtyao/LOTUS/blob/master/docs/project_showcase.md)
· [Results and protocol](https://github.com/elvisxtyao/LOTUS/blob/master/docs/t08_test_results.md)
· [Architecture](https://github.com/elvisxtyao/LOTUS/blob/master/docs/architecture.md)
· [Current scope](https://github.com/elvisxtyao/LOTUS/blob/master/docs/project_status.md)

*The walkthrough uses saved results; there is no live public service.*

### [Where Does Hebbian Learning Help?](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder)

A PyTorch study of **how learning rules shape representation diversity**, comparing local Hebbian learning with backpropagation in a three-layer MNIST autoencoder.

| Research | Engineering |
| :--- | :--- |
| Compared Hebbian, backpropagation, and hybrid encoders using **five paired seeds** and matched random-prefix controls. | Built modular training and evaluation code, automated tests, and deterministic release archives. |
| Adding backpropagation at the deepest encoder layer increased mean effective rank (a measure of representation diversity) from **1.02 to 11.54** in the tested setup. | Added CI checks for saved experiment evidence and figures, with a demo that requires no model training. |

**Explore the findings →** [3–5 minute walkthrough](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/project_demo.ipynb) · [Results](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/RESULTS_SUMMARY.md)

**Inspect the engineering →** [Implementation](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/tree/main/training) · [Tests](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/tree/main/tests) · [Reproduce](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/REPRODUCIBILITY.md)

## Tools I use

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
