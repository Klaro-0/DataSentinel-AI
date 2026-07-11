<div align="center">

# ▣ DataSentinel AI

### Your model isn't broken. Your data is.

Automated data quality intelligence for machine learning — catch label errors, duplicates, outliers, drift, and annotation conflicts before they train into your model.

[![Python](https://img.shields.io/badge/Python-3.10+-4FD1B8?style=flat-square&logo=python&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-Apache%202.0-F0A63D?style=flat-square)](#license)
[![PyPI](https://img.shields.io/badge/pip-datasentinel--ai-4FD1B8?style=flat-square&logo=pypi&logoColor=white)](#installation)
[![Status](https://img.shields.io/badge/Status-Active-4FD1B8?style=flat-square)](#roadmap)
[![Maintainer](https://img.shields.io/badge/Maintainer-Yahi%20Abdelhak-1a1a1a?style=flat-square)](#author)

[Quick Start](#-quick-start) · [Features](#-what-it-catches) · [Architecture](#-architecture) · [Applications](#-example-applications) · [Roadmap](#-roadmap)

</div>

<br>

```diff
- Collect data → Train model → Tune → Deploy               (errors baked in)
+ Collect data → Audit dataset → Repair → Train → Deploy   (errors caught first)
```

<br>

## ◆ Why this exists

Most ML failures trace back to the dataset, not the model. DataSentinel is a data-centric
framework that inspects any dataset — image, text, audio, tabular, or multimodal — and
returns a ranked report of what's silently wrong with it.

<br>

## ▣ Quick Start

```bash
pip install datasentinel-ai
```

```python
from datasentinel import DataAudit

audit = DataAudit(dataset)
audit.find_issues(embeddings=embeddings, predictions=pred_probs)
audit.report()
```

<details>
<summary><strong>▸ Output</strong></summary>

<br>

| Metric | Result |
|---|---|
| Potential label errors | `124` |
| Duplicates detected | `37` |
| Outliers identified | `18` |
| Low-confidence samples | `92` |
| **Dataset quality score** | **`87.3 / 100`** |

</details>

<br>

## ◇ What it catches

| | Check | Description |
|---|---|---|
| 🏷️ | **Label quality** | Ranks likely mislabeled samples using model confidence + representation learning |
| 🧬 | **Duplicates** | Finds exact and semantic near-duplicates inflating your metrics |
| 📍 | **Outliers** | Flags abnormal records and distribution anomalies |
| 📉 | **Dataset drift** | Tracks divergence between training and production data over time |
| ✎ | **Annotation audit** | Measures inter-annotator agreement and labeling consistency |
| ↺ | **Active learning** | Recommends exactly which samples to review next, in priority order |

<br>

## ▣ Architecture

```mermaid
flowchart TD
    A["Dataset — images · text · audio · tabular · multimodal"] --> B["Feature Extraction"]
    B --> C["Quality Analysis Engine"]
    C --> D1["Label Audit"]
    C --> D2["Duplicate Detection"]
    C --> D3["Outlier Analysis"]
    C --> D4["Drift Detection"]
    C --> D5["Confidence Scoring"]
    D1 & D2 & D3 & D4 & D5 --> E["Issue Report"]
    E --> F["Dataset Improvement"]

    style C fill:#0A0D12,stroke:#4FD1B8,color:#4FD1B8
    style F fill:#0A0D12,stroke:#F0A63D,color:#F0A63D
```

<br>

## ◆ Supported data & frameworks

<table>
<tr><td valign="top" width="50%">

**Data types**

| Type | Support |
|---|---|
| Images | ✅ |
| Text | ✅ |
| Audio | ✅ |
| Tabular | ✅ |
| Time series | ✅ |
| Multimodal | ✅ |

</td><td valign="top" width="50%">

**Frameworks**

- PyTorch · TensorFlow · Keras
- Scikit-Learn · XGBoost · LightGBM
- Hugging Face Transformers
- OpenAI Embeddings
- Custom models

</td></tr>
</table>

<br>

## ▣ Example Applications

<details>
<summary><strong>🖼️ Computer Vision</strong></summary>
<br>

- Catches incorrect image labels before they skew training
- Finds duplicate images across train / val / test splits
- Surfaces class imbalance hidden inside large image sets

</details>

<details>
<summary><strong>💬 Natural Language Processing</strong></summary>
<br>

- Flags annotation mistakes in labeled text corpora
- Detects intent classification inconsistencies
- Audits named entity labeling for systematic errors

</details>

<details>
<summary><strong>🛡️ Security Analytics</strong></summary>
<br>

- Validates log datasets before they train detection models
- Assesses threat intelligence feed quality at ingestion
- Audits anomaly-detection training sets for label drift

</details>

<details>
<summary><strong>🏥 Healthcare AI</strong></summary>
<br>

- Verifies medical annotations against inter-rater agreement
- Monitors dataset consistency across collection sites

</details>

<br>

## ◇ Roadmap

- [x] Label error detection
- [x] Duplicate detection
- [x] Outlier analysis
- [x] Dataset reporting
- [ ] Dataset repair suggestions
- [ ] Human-in-the-loop review
- [ ] Dataset governance dashboard
- [ ] Multi-annotator intelligence
- [ ] Enterprise monitoring

<br>

## ▣ Research foundations

`Data-Centric AI` · `Representation Learning` · `Weak Supervision` · `Active Learning` · `Outlier Detection` · `Dataset Governance` · `Trustworthy AI`

<br>

---

<div align="center">

### Author

**Yahi Abdelhak**
Cybersecurity Researcher · AI Engineer

Apache License 2.0 — see [`LICENSE`](#license)

⭐ **Star this repo** if DataSentinel AI helped clean up your dataset.

</div>
