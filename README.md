# AI-Driven Explainable Credit Risk Modelling Using 2D Image CNNs and Network Graphs

**Intern — Advanced Quantz & Analytics (AQuA) | BFSI Vertical | Tata Consultancy Services (TCS), Pune**
*May 2026 – July 2026*

## 📌 Overview

This project presents an end-to-end, explainable credit risk modelling pipeline built on the AMEX time-series dataset. It combines large-scale feature engineering on Databricks, advanced feature selection (including CNN-based permutation importance and graph-based interaction analysis via Neo4j), imbalance handling with generative techniques, and a suite of boosting/deep learning models — all wrapped in a layer of explainability (SHAP, LIME, DiCE, GenAI) to produce audit-ready credit risk reports. Results were operationalized through a Power BI dashboard and an automated n8n workflow triggering emails on loan applications.

## 🚀 Key Highlights

- **0.98 ROC-AUC** and **93% precision** on the final model
- Probability of Default (PD) converted into an interpretable **CIBIL-style credit score**
- Fully automated pipeline: **loan application → risk scoring → audit report → email notification**
- Explainability baked in at every stage (feature-level and prediction-level)

## 🏗️ Architecture & Workflow

### 1. Data Engineering
- Built a **Databricks Medallion Architecture (Bronze → Silver → Gold)** in **PySpark** on the AMEX time-series dataset
- Extensive feature creation with **Feature Store** integration for reusable, versioned features

### 2. Feature Engineering & Analysis
- **Univariate, Bivariate, and Multivariate Analysis**
- **Correlation Filtering**, **Factor Analysis**, and **Clustering** for redundancy reduction and pattern discovery

### 3. Feature Selection
- Ranked features using:
  - **SHAP**
  - **Boruta**
  - **Genetic Algorithm**
  - **CNN Permutation Importance**
- Analyzed **feature interactions** using **Neo4j** graph modelling

### 4. Class Imbalance Handling
- Addressed skewed class distribution using **ADASYN** and **CTGAN** (synthetic minority oversampling)

### 5. Model Development & Tuning
- Compared multiple algorithms:
  - Logistic Regression (LR)
  - **LightGBM**
  - **XGBoost** — best-performing model
  - CatBoost
  - Dense Neural Network
- Hyperparameter tuning via **Optuna**

### 6. Explainability & Reporting
- Converted **Probability of Default (PD)** into a **CIBIL Score**
- Generated audit-ready reports using:
  - **SHAP** (global & local feature attribution)
  - **LIME** (local interpretability)
  - **DiCE** (counterfactual explanations)
  - **GenAI** (natural-language explanation generation)

### 7. Visualization & Automation
- Built an interactive **Power BI dashboard** for risk monitoring
- Orchestrated an **n8n** workflow automating the pipeline from **customer loan application → risk scoring → email trigger**, integrated using **FastAPI** and **ngrok**

## 🛠️ Tech Stack

| Category | Tools / Libraries |
|---|---|
| Big Data & Engineering | Databricks, PySpark, Feature Store |
| Feature Selection | SHAP, Boruta, Genetic Algorithms, CNN Permutation Importance |
| Graph Analysis | Neo4j |
| Imbalance Handling | ADASYN, CTGAN |
| Modelling | Logistic Regression, LightGBM, XGBoost, CatBoost, Dense Neural Networks |
| Hyperparameter Tuning | Optuna |
| Explainability | SHAP, LIME, DiCE, GenAI |
| Visualization | Power BI |
| Automation & Orchestration | n8n, FastAPI, ngrok |

## 📊 Results

| Metric | Score |
|---|---|
| ROC-AUC | 0.98 |
| Precision | 93% |
| Best Model | XGBoost |

.........................................................................................................................................

## ⚙️ How It Works (End-to-End Flow)

1. Customer submits a loan application
2. Data flows through the Databricks Medallion pipeline for feature computation
3. Model (XGBoost) predicts Probability of Default
4. PD is converted to a CIBIL-style score
5. Explainability layer generates an audit-ready report (SHAP/LIME/DiCE/GenAI)
6. FastAPI serves the prediction; n8n orchestrates the workflow
7. Email notification is triggered to relevant stakeholders
8. Power BI dashboard reflects updated risk metrics

## 🔮 Future Enhancements

- Extend 2D Image CNN representation of transaction sequences for deeper pattern recognition
- Real-time streaming feature computation
- Model monitoring and drift detection dashboard

## 👤 Author

Intern, Advanced Quantz & Analytics (AQuA), BFSI
Tata Consultancy Services (TCS), Pune

---
*This project was developed during a summer internship (May 2026 – July 2026) as part of TCS's Advanced Quantz & Analytics team within the BFSI vertical.*
