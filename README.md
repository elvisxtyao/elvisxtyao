# Theo (Xiaotian) Yao

**Machine Learning · Software Engineering · AI**

I explore how neural networks learn and build reproducible software to evaluate them.
Currently seeking MLE, SDE, and AI engineering roles.

[LinkedIn](https://www.linkedin.com/in/xiaotian-yao/) · [LOTUS quickstart](https://github.com/elvisxtyao/LOTUS/blob/master/docs/installation.md) · [Hebbian learning demo](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/project_demo.ipynb)

## Selected work

### [LOTUS — Learning single-cell dynamics](https://github.com/elvisxtyao/LOTUS)

A PyTorch project for **modeling single-cell dynamics with incomplete lineage labels**, from reproducible evaluation to CPU model serving.

| Research | Engineering |
| :--- | :--- |
| Compared **seven methods across three training seeds** on held-out LARRY cells within seen clones (Day 4→6; one split). | Built train-fitted preprocessing, resumable training, MLflow tracking, and shared CLI/FastAPI inference. |
| MLP and ridge achieved lower endpoint error than all three dynamics variants in the fixed-budget comparison. | Verified **2,718 error-free requests** with local Docker CPU serving. Deployed a **synthetic model on AWS EC2**, validating monitoring, fault recovery, and release rollback. |

**Explore the findings →** [Results and figures](https://github.com/elvisxtyao/LOTUS#results) · [Evaluation report](https://github.com/elvisxtyao/LOTUS/blob/master/docs/t08_test_results.md)

**Inspect the engineering →** [Implementation](https://github.com/elvisxtyao/LOTUS/tree/master/src/dynenc) · [Tests](https://github.com/elvisxtyao/LOTUS/tree/master/tests) · [AWS deployment](https://github.com/elvisxtyao/LOTUS/blob/master/docs/cloud_cpu_deployment.md) · [Reproduce](https://github.com/elvisxtyao/LOTUS/blob/master/docs/reproducibility.md)

### [Where Does Hebbian Learning Help?](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder)

A PyTorch study of **how learning rules shape representation diversity**, comparing local Hebbian learning with backpropagation in a three-layer MNIST autoencoder.

| Research | Engineering |
| :--- | :--- |
| Compared Hebbian, backpropagation, and hybrid encoders using **five paired seeds** and matched random-prefix controls. | Built modular training and evaluation code, automated tests, and deterministic release archives. |
| Adding backpropagation at the deepest encoder layer increased mean effective rank (a measure of representation diversity) from **1.02 to 11.54** in the tested setup. | Added CI checks for saved experiment evidence and figures, with a demo that requires no model training. |

**Explore the findings →** [3–5 minute walkthrough](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/project_demo.ipynb) · [Results](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/RESULTS_SUMMARY.md)

**Inspect the engineering →** [Implementation](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/tree/main/training) · [Tests](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/tree/main/tests) · [Reproduce](https://github.com/elvisxtyao/neuroai-hebbian-vs-backprop-autoencoder/blob/main/REPRODUCIBILITY.md)

## Tools I use

**ML & data**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)

**Model delivery**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)
![DVC](https://img.shields.io/badge/DVC-945DD6?style=flat&logo=dvc&logoColor=white)

**Cloud & quality**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat&logo=terraform&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
