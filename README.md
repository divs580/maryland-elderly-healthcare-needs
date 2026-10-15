# 👵 Identifying Key Healthcare Assistance Needs for Older Adults in Maryland

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python)](./)
[![PySpark](https://img.shields.io/badge/PySpark-3.5.4-E25A1C?logo=apachespark)](./)
[![Machine Learning](https://img.shields.io/badge/Unsupervised%20ML-K--Means%20Clustering-F7931E)](./)
[![Domain](https://img.shields.io/badge/Domain-Population%20Health%20%26%20Informatics-2EA44F)](./)

## 📌 Executive Summary
Analyzed synthetic EHR datasets encompassing **53,068 patient records** across 16 relational clinical tables to assist the Maryland state government in optimizing elderly healthcare assistance under strict budgetary constraints. By focusing on adults aged 65 and older (representing **73.6% / 39,070 patients** of the cohort), this study quantifies extreme out-of-pocket coverage deficits, surfaces high-frequency chronic conditions, evaluates medication cost drivers, and uses **PySpark K-Means clustering** to segment vulnerable populations for targeted state interventions.

### 📄 Project Deliverables
* [📑 Executive Policy Brief & State Recommendations (PDF)](./healthcare_need_analysis_report.pdf)
* [📓 PySpark & Python Analysis Pipeline (Jupyter Notebook)](./healthcare_need_analysis.ipynb)

---

## 🔑 Key Population Health Benchmarks

| Metric | Observed Benchmark | Public Health & Policy Implication |
| :--- | :--- | :--- |
| **Analyzed Cohort** | 53,068 total records (39,070 aged 65+) | Senior adults represent 73.6% of patient population |
| **Average Senior Care Cost** | $1,274,091.44 | High cumulative lifetime spend driven by comorbidity management |
| **Average Insurance Coverage** | $22,135.69 (1.74% of expenses) | Severe coverage deficit leaving massive out-of-pocket financial liability |
| **Average Coverage Gap** | $1,251,955.75 per senior patient | Extreme underinsurance exposure requiring state-level safety nets |
| **Peak Vulnerability Window**| Ages 90 – 94 ($1,276,866 gap) | Widest absolute dollar gap between clinical expenses and coverage |
| **Top Procedure Cost Drivers**| Lung Transplant ($514,984) / ICU ($264,601) | Critical acute episodes drive disproportionate financial strain |

---

## 🎯 Key Analytical Findings

### 1. The Catastrophic Coverage Deficit
* Despite average lifetime healthcare expenses exceeding **$1.27M**, insurance mechanisms covered a mean of only **$22,135 (1%–4% of total charges)**.
* Even in the best-covered demographic bands, the average out-of-pocket exposure exceeded **$1.22M per elderly patient**.

### 2. High-Frequency Chronic Conditions vs. Out-of-Pocket Medications
* **Top Clinical Conditions:** Viral sinusitis (43,745 cases), acute viral pharyngitis (24,046 cases), obesity / BMI 30+ (23,089 cases), and prediabetes (20,396 cases).
* **Medication Burdens:** Routine daily maintenance prescriptions—such as *Hydrochlorothiazide 25 MG*, *Lisinopril 10 MG*, and *Amlodipine 2.5 MG*—dominate senior prescription volume, while specialty treatments like *Humulin Insulin* ($206.34/fill out-of-pocket) create severe recurring financial toxicity.

### 3. Patient Segmentation (Unsupervised PySpark K-Means Clustering)
Feature engineering combined normalized age, healthcare expenses, and coverage into 4 distinct risk tiers:
* **Cluster 0 (Younger Seniors, High Spend):** Mean age 73.9, high average expenses ($1.44M), only 1% coverage ($11,020).
* **Cluster 1 (Oldest-Old, Critical Need):** Mean age 91.7, highest patient count (19,523 seniors), $1.50M in expenses with a $1.48M gap.
* **Cluster 2 (Moderate Need):** Mean age 85.9, lower expenses ($226K) with 7% coverage ratio.
* **Cluster 3 (High-Coverage Outliers):** Mean age 93.6, highest expenses ($1.58M) paired with significant coverage ($271K / 17%).

### 4. County-Level Health Disparities
Geographic gap mapping identified the ten most vulnerable jurisdictions in Maryland, led by:
1. **Charles County:** $1,354,272 average coverage gap (844 seniors)
2. **Queen Anne's County:** $1,354,216 average coverage gap (167 seniors)
3. **Howard County:** $1,337,859 average coverage gap (2,208 seniors)

---

## 💡 Strategic Policy Recommendations for Maryland State Leadership

| Priority Area | Target Population | Actionable Strategy |
| :--- | :--- | :--- |
| **Targeted Medication Subsidies** | Seniors on maintenance therapy (Insulin, Epogen, Metformin) | Establish state copay caps and subsidized prescription pools to prevent medication abandonment and emergency complications. |
| **Geographic Mobile Health Units** | Charles, Queen Anne's, and Howard Counties | Deploy state-funded mobile screening and preventive clinics to rural and high-gap counties to address obesity and prediabetes early. |
| **Catastrophic Age-Tier Relief** | Seniors Aged 85 – 94 (Clusters 0 & 1) | Create graduated supplemental gap assistance specifically targeting the oldest-old experiencing over $1.4M in medical debt exposure. |

---

## 📁 Repository Structure
```text
├── README.md                           <-- Project case study, findings, and policy recommendations
├── healthcare_need_analysis_report.pdf  <-- Executive report prepared for Maryland state officials
└── healthcare_need_analysis.ipynb      <-- PySpark & Pandas data pipeline, EDA, and K-Means modeling
