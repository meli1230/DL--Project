# Machine-Generated Code Detection

This project investigates machine-generated code detection in multilingual settings, focusing on cross-language generalization and structural robustness. The study compares a classical baseline (TF-IDF + Logistic Regression) with neural code encoders (CodeBERT and GraphCodeBERT) to evaluate how well models distinguish between human-written and LLM-generated code, especially when evaluated on unseen programming languages. 

The repo also includes the submitted project paper, developed with the structure of an academic article in mind. 

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

## Models evaluated 
###
