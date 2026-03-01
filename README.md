# Machine-Generated Code Detection

This project investigates machine-generated code detection in multilingual settings, focusing on cross-language generalization and structural robustness. The study compares a classical baseline (TF-IDF + Logistic Regression) with neural code encoders (CodeBERT and GraphCodeBERT) to evaluate how well models distinguish between human-written and LLM-generated code, especially when evaluated on unseen programming languages. 

The repo also includes the submitted project paper, developed with the structure of an academic article in mind. 

## Research Objectives
- `RQ1`: How well do classical and neural models perform when trained and tested on the same languages?
- `RQ2`: How does performance change when evaluated on unseen programming languages?
- `RQ3`: Does incorporating structural code information (data flow) improve cross-language robustness?
- *Supplementary Analysis*: Does code length bias model predictions?
