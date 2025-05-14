# 📈 Modeling Daily Associations Between Self-Injurious Urges and Behaviors Using Ecological Momentary Assessment
Using generalized linear modeling (also known as multilevel models or mixed-effect models) to examine the predictive value of various urge characteristics on self-injurious behaviors. 

---

**Conference Project Title:** Prospective Associations Between Self-Injurious Urges and Behaviors  
**Authors:** Madeline M. Navea, Jannah R. Moussaoui, April R. Smith, Elizabeth A. Velkoff  
**Conferences Presented Work At:** Suicide Research Symposium (Virtual) 2025

---

## 🔍 Overview

The **urge** to engage in a self-injurious behavior is arguably the **strongest predictor** for **self-injurious behavior**s. However, specific characteristics of urges (intensity and frequency) may not predict all characteristics of self-injurious behaviors (frequency, duration, engagement). This project explores the relationship between characteristics of self-injurious urges (SIUs) and self-injurious behaviors (SIBs) using ecological momentary assessment (EMA) data collected in **real time** over 14 days. The project applies **generalized linear mixed models (GLMMs)** to assess whether the **intensity and frequency** of SIUs can **predict** daily engagement in, and characteristics of, SIBs.

The goal of this project is to understand the **within-subject, time-sensitive predictive signals** of high-risk behavior using interpretable and generalizable statistical models, with the broader aim of supporting **real-time intervention strategies**.

---

## 📊 Research Questions

- Do same-day **SIU intensity** and **SIU frequency** predict the likelihood of engaging in a SIB?
- Can SIU characteristics predict **how long** or **how often** SIBs occur once initiated?
- What are the limitations of using subjective urge measures to infer behavioral patterns?

---

## 🧠 Data Description

- **Participants:** N = 124 individuals reporting ≥3 SIBs in the prior month
- **Duration of Study:** 14-day ecological momentary assessment (EMA)
- **Survey Frequency:** Daily (self-reported)
- **Data Points Collected:**
  - Predictors:
    - **SIU Intensity:** 0–100 scale (standardized)
    - **SIU Frequency:** Count per day (standardized)
  - Outcomes:
    - **SIB Engagement:** Binary (Yes/No)
    - **SIB Frequency:** Daily count
    - **SIB Duration:** Minutes

> ⚠️ **Note**: Data that support the findings of this study are available from the corresponding authors upon reasonable request. Code and data visualizations are available to download.

---

## 📦 Repository Structure

📁 data/ <- Simulated EMA dataset
📁 notebooks/ <- Jupyter notebooks for EDA, model fitting, and visualization
📁 models/ <- GLMM specifications and diagnostics
📁 scripts/ <- Preprocessing and standardization logic
📄 requirements.txt <- Python environment dependencies
📄 README.md <- Project overview and structure

---

## 🔍 Methods

- **Model Type:** Generalized Linear Mixed Models (GLMMs)
- **Fixed Effects:** SIU intensity, SIU frequency (standardized)
- **Random Effects:** Participant ID
- **Dependent Variables:**
  - SIB Engagement (binary logistic)
  - SIB Frequency (Poisson/negative binomial)
  - SIB Duration (continuous or log-normal, exploratory)

### R Packages Used

- `tidyverse`, `magrittr` for data wrangling  
- `lme4`, `modelsummary` for GLMMs  
- `ggplot2`, `wesanderson` for visualization

---

## 📈 Key Results

- **SIU Intensity** was a strong predictor of **SIB engagement**:  
  - OR = 7.36, 95% CI [3.73, 14.50]  
- **SIU Frequency** was a strong predictor of **SIB engagement**:  
  - OR = 9.31, 95% CI [4.40, 19.69]  
- **No significant association** between SIU variables and either:
  - **SIB duration**
  - **SIB frequency**

These findings suggest that while **urge characteristics predict SIB engagement**, they may not reliably inform about **behavioral severity** like the amount of times you engage in a behavior or for how long. This is possibly due to its habitual nature or differing subjective thresholds for relief.

---

## 💡 Future Directions

- Apply **time-series or hierarchical Bayesian models** to explore individual variability over time
- Incorporate **affective state** or **interoceptive awareness** data for multivariate prediction
- Develop **risk scoring systems** for real-time alerts in mobile health (mHealth) applications
- Explore **causal modeling** using Granger causality or dynamic structural models

---

## 📜 Citation

Navea M.M., Moussaoui J.R., Smith A.R., Velkoff E.A. (2025, April). Prospective Associations Between Self-Injurious Urges and Behaviors. Data blitz at the fourth annual Suicide Research Symposium, Virtual.

