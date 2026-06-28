# 🎓 Student Participation Prediction
### AI-Powered Data Analysis | RIT × Excelerate Internship | May–Jun 2026

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3-orange.svg)](https://scikit-learn.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📌 Project Overview

This project was built during a 4-week AI-Powered Data Analysis internship at the **Rochester Institute of Technology (RIT)** in collaboration with **Excelerate**. The goal was to analyze student participation data across 22 opportunities on the Excelerate platform and build a machine learning model to **predict whether a student will participate** in a given opportunity.

**Dataset:** 8,558 student-opportunity records | 22 unique opportunities | 71 countries | 2022–2024

---

## 🎯 Problem Statement

The Excelerate platform hosts 5 types of opportunities: Internships, Courses, Events, Competitions, and Engagement activities. Despite internships accounting for **63% of all applications**, only **21.5%** of students who apply actually participate. The goal was to:

1. Understand **what drives student participation**
2. Build a model to **predict participation probability** for each opportunity
3. Provide **actionable recommendations** to improve platform outcomes

---

## 📁 Project Structure

```
Excelerate-Internship/
│
├── data/
│   └── README_data.md          # Dataset description (raw data not included)
│
├── notebooks/
│   ├── Week1_Data_Understanding.ipynb
│   ├── Week2_EDA_Cohort_Analysis.ipynb
│   ├── Week3_ML_Models.ipynb
│   └── Week4_Final_Analysis.ipynb
│
│
├── outputs/
│   └── predicted_probabilities.csv   # Model output for all 22 opportunities
│
│
├── requirements.txt
└── README.md
```

---

## 🔄 Week-by-Week Breakdown

### Week 1 — Data Understanding
- Loaded and audited the raw dataset (8,558 rows × 17 columns)
- Identified missing values, data types, and inconsistencies
- Mapped all 8 application statuses and 5 opportunity categories
- Defined the binary target variable: `Is_Placed` (1 = Team Allocated / Started / Rewards Award)

### Week 2 — EDA & Cohort Analysis
- Engineered 10 new features (Age, Days_to_Apply, Has_Start_Date, etc.)
- Discovered: internships have a 65.8% rejection rate vs near-zero for events
- Found that `Days_to_Apply` is the strongest behavioral signal (placed avg: 10.8 days vs rejected avg: 84 days)
- Performed geographic and gender cohort analysis across 71 countries

### Week 3 — Machine Learning Models
- Trained 3 models: Logistic Regression, Gradient Boosting, Random Forest
- **Selected Random Forest** (AUC-ROC: 0.9114, Accuracy: 85.6%)
- Generated predicted participation probabilities for all 22 opportunities
- Feature importance analysis: program design >> student demographics

### Week 4 — Final Analysis & Recommendations
- Delivered 5 strategic recommendations to the Excelerate team
- Built a 7-metric measurement framework for future cohorts
- Identified Career Essentials (94.4%, 1,423 applicants) as the platform benchmark

---

## 📊 Key Findings

| Finding | Detail |
|---|---|
| Internship participation rate | 21.5% (lowest category) |
| Events/Engagement participation rate | 96–97% |
| Top behavioral signal | Apply within 14 days → 2x placement rate |
| Top predictive features | Historical Participation Rate (48.5%) + Opportunity Category (28.6%) |
| Best ML model | Random Forest — AUC-ROC: 0.9114, Accuracy: 85.6% |
| Gender insight | Female applicants outperform males by 4.6pp despite 41% enrollment share |
| Geographic outlier | Egyptian (78%) and Kenyan (74%) learners outperform global average |

---

## 🤖 Model Performance

| Model | AUC-ROC | Accuracy | F1-Score |
|---|---|---|---|
| Logistic Regression | 0.900 | 83.99% | — |
| Gradient Boosting | 0.9107 | 84.99% | — |
| **Random Forest ★** | **0.9114** | **85.57%** | **90.2%** |

Random Forest was chosen for its superior AUC, native feature importance, and stable cross-validation variance (±0.012).

---

## 🛠️ How to Run

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/student-participation-prediction.git
cd student-participation-prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run notebooks in order
jupyter notebook notebooks/Week1_Data_Understanding.ipynb
```

> ⚠️ The raw dataset is proprietary to Excelerate and is not included. The code is structured to work with any similarly formatted CSV.

---

## 📦 Requirements

```
pandas>=1.5.0
numpy>=1.23.0
scikit-learn>=1.3.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0
xgboost>=1.7.0
```

---

## 👤 Author

**Nidhi Jain** | AI Data Analyst Intern  
RIT × Excelerate AI-Powered Data Analysis Internship  
May–June 2026 | Overall Performance: **94%**

---

## 📄 License

This project is for educational purposes. Dataset is proprietary to Excelerate.
