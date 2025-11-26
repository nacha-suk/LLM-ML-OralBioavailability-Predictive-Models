# LLM-ML-OralBioavailability-Predictive-Models

## Integrating LLM-Accelerated Data Acquisition with Explainable ML to Predict Pharmacokinetic Parameters ($AUC, C_{max}, T_{max}$)

This repository showcases my Master's Dissertation project from the Jagiellonian University Medical College, Chair of Pharmaceutical Technology and Biopharmaceutics.

The project introduces an innovative, dual-fingerprint approach to **Pharmacokinetics (PK) prediction** by leveraging **Large Language Models (LLMs)** to overcome the data bottleneck in traditional drug development.

---

## 🎯 The Research Problem (The Gap)

Current predictive models for oral bioavailability $\mathbf{(AUC, C_{max}, T_{max})}$ struggle for two critical reasons:

1.  **Neglect of Formulation:** They typically focus only on the drug's molecular properties, overlooking the crucial influence of the **dosage form's characteristics** (e.g., controlled release).
2.  **Manual Bottleneck:** Traditional data collection from unstructured scientific literature is a **slow, manual, and unscalable bottleneck**.

---

## ✨ Methodology & Technical Innovation

This project was engineered to solve the data scarcity and feature incompleteness problems, highlighting my skills in MLOps, LLM integration, and XAI.

### 1. LLM-Accelerated Data Pipeline (Data Engineering)

* Developed a novel workflow using **Google NotebookLM** for intelligent article pre-selection.
* Employed **Gemini 2.5 Pro** for the **automated, high-throughput extraction** of complex $\mathbf{PK}$ and $\mathbf{Formulation}$ data from thousands of unstructured literature sources (PDFs, abstracts, full-text articles).

### 2. Dual Feature Engineering (Domain Expertise)

The models were trained on a unique combination of features (the "Dual Fingerprint"):

* **Molecular Fingerprint:** Calculated physicochemical descriptors (e.g., $logP$, TPSA) via a dedicated API.
* **Dosage Form Fingerprint:** Novel representation of drug release characteristics using $\mathbf{T(Q\%)}$ values to capture the *in vitro-in vivo* correlation (IVIVC).

### 3. Advanced Modeling & Validation (MLOps)

* **Modeling:** Used **AutoML ($\mathbf{H2O.ai}$)** for efficient, high-performance model selection.
* **Rigor:** Implemented **Leave-One-Group-Out (LOGO)** cross-validation to ensure rigorous, leakage-free validation that respects the inherent grouping in the data.

---

## 📈 Key Findings & Critical Analysis

The results provide a dual perspective: a success story in data scaling and a critical diagnosis of data bias using Explainable AI.

### Success in Scaling: $T_{max}$ Prediction

* The LLM-accelerated pipeline successfully **expanded the training dataset by 150\%**.
* This led to a significant improvement in $\mathbf{T_{max}}$ prediction, achieving an **AutoML $\mathbf{R^2}$ of 0.845** (compared to an $R^2$ of 0.584 on the original manual dataset).

### Critical Failure of Generalization: $C_{max}$ Prediction

* The crucial **cross-dataset validation** (testing the LLM-trained model on the manual dataset) revealed a severe generalization failure for $\mathbf{C_{max}}$ prediction.
* The model yielded a **negative $\mathbf{R^2}$ of -1.900**, indicating it learned specific noise patterns from the LLM-generated data that were detrimental to real-world performance.

### XAI Diagnosis (Explainable AI)

* **SHAP** and **Partial Dependence Plots (PDPs)** confirmed that the **LLM-trained $\mathbf{C_{max}}$ model learned fundamentally different feature relationships** (e.g., the relationship between a specific molecular descriptor and $C_{max}$) than the model trained on the manually curated data.
* This XAI-driven finding led to the diagnosis of **systematic data bias** introduced by the LLM extraction process, which is a critical insight for future LLM-in-science applications.

---

## 🛠️ Career-Strategic Skills Demonstrated

| Category | Skills / Technologies |
| :--- | :--- |
| **Data Engineering** | LLM Integration ($\mathbf{Gemini\ 2.5\ Pro}$), Automated Data Extraction, Data Pipeline Development, API Integration |
| **Machine Learning** | AutoML ($\mathbf{H2O.ai}$), Regression Modeling, Advanced Cross-Validation ($\mathbf{LOGO}$), MLOps Principles |
| **Explainable AI** | $\mathbf{SHAP}$ (SHapley Additive exPlanations), Partial Dependence Plots ($\mathbf{PDPs}$), Feature Importance Analysis, Model Diagnosis |
| **Domain Expertise** | Pharmacokinetics ($\mathbf{AUC, C_{max}, T_{max}}$), Pharmaceutical Formulation Science, IVIVC, Medicinal Chemistry |

---
