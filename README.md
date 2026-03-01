# Machine-Generated Code Detection

This project investigates machine-generated code detection in multilingual settings, focusing on cross-language generalization and structural robustness. The study compares a classical baseline (TF-IDF + Logistic Regression) with neural code encoders (CodeBERT and GraphCodeBERT) to evaluate how well models distinguish between human-written and LLM-generated code, especially when evaluated on unseen programming languages. 

The repo includes the collab notebook, as well as the submitted project paper, developed with the structure of an academic article in mind. 

---

## Research Objectives
- `RQ1`: How well do classical and neural models perform when trained and tested on the same languages?
- `RQ2`: How does performance change when evaluated on unseen programming languages?
- `RQ3`: Does incorporating structural code information (data flow) improve cross-language robustness?
- **Supplementary Analysis**: Does code length bias model predictions?

---

## Dataset
In this project, we use a subset of the *SemEval Co-Det-M4 benchmark*, designed for multilingual machine-generated code detection.

### Seen Languages (train / validation)
- Python
- Java
- C++

### Unseen Languages (test)
- Go
- PHP
- C#
- C
- JavaScript

This task is formed as a binary classification problem, classifying the given code snippet as either human-written or machine-generated.

---

## Implementation

### Models Evaluated
- TF-IDF with Logistic Regression
- CodeBERT
- GraphCodeBERT

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- Macro-F1 (main comparison metric)

Macro-F1 is emphasized due to potential class imbalance and multilingual variability.

---

## Key Findings

### In-Distribution (Seen Languages)
- TF-IDF baseline performs strongly
- CodeBERT achieves near-perfect performance
- Neural models significantly outperform classical methods

### Cross-Language Generalization (Unseen Languages)
- Severe performance drop across all models
- Surface-level cues do not transfer well
- Neural models are more robust but still struggle

### Structural Modeling
- GraphCodeBERT consistently improves performance over CodeBERT on most unseen languages
- Improvements are moderate and language-dependent
- PHP remains especially difficult

### Length Bias
Behavioral analysis on a large unlabeled dataset shows:
- Longer code snippets are more likely to be predicted as machine-generated
- TF-IDF exhibits the strongest bias
- GraphCodeBERT reduces but does not eliminate this effect

### Limitations
- Training languages limited to three (Python, Java, C++)
- Colab environment constrained batch size and training time
- Binary classification only (no hybrid/partially-assisted detection)
- No adversarial robustness testing
