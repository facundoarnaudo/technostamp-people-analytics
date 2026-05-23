# TechnoStamp Industries: People Analytics & Operations Optimization

## 📌 Project Overview
This project focuses on transforming raw HR data into actionable business insights for TechnoStamp Industries, a manufacturing company with 450 employees. The goal is to move from intuition-based HR decisions to a data-driven strategy, optimizing operational efficiency, talent retention, and workplace safety.

> **🌐 Note on Language:** While this documentation and the executive summary are presented in English to reach a broader audience, the underlying dataset, Python code (variables/comments), and raw outputs are in Spanish, reflecting the real-world operational context of the company.

## 🎯 Business Problem
The executive board needed clear answers to critical operational questions:
* What is the true financial and operational cost of overtime?
* What is the ROI of our training programs?
* Are there gender disparities in compensation and career advancement?
* Is our critical talent at risk of retirement without a succession plan?

## 🛠️ Tech Stack & Tools
* **Language:** Python
* **Data Manipulation & Cleaning:** Pandas, NumPy
* **Data Visualization:** Seaborn, Matplotlib
* **Environment:** Jupyter Notebook

## 💡 Key Findings & Business Impact
Through rigorous data cleaning, cross-validation, and exploratory data analysis (EDA), the following insights were uncovered:

* **Safety & Hidden Costs:** Overtime is directly correlated with workplace accidents. Working more than 5 hours of overtime monthly decreases production quality (higher scrap rate) and generates an estimated **$7.8M in hidden costs** (direct medical costs + indirect lost wages) over 1.5 years.
* **Training ROI:** Employees who completed safety training showed a **~60% reduction in accident probability**. Technical training also proved to increase production volume while maintaining low scrap rates.
* **Equity & Culture (Glass Ceiling):** While there is pay equity at entry levels, female representation drops significantly in leadership roles. Furthermore, the gender pay gap widens to **6.8%** in upper operational management, primarily driven by bonus distributions rather than base salary.
* **Succession Planning:** An automated logic was applied to identify retirement risks. Fortunately, there are no "Red Alerts" (critical retirements in < 12 months). However, a "Yellow Alert" (12-24 months) was identified in the Stamping area, and the system successfully mapped an internal successor with 10 years of experience.

## ⚙️ Methodology & Data Wrangling
Real-world data is rarely perfect. The data preparation phase included:
* **Character Encoding Fixes:** Engineered a recursive text-cleaning function to handle Latin-1 encoding errors.
* **Historical Validation:** Recalculated dynamic variables such as exact age, seniority, and retirement projections using a strict cutoff date.
* **Cross-Referencing:** Merged snapshot data (Headcount) with transactional data (Events and Training) to audit discrepancies and measure real-world absenteeism versus reported data.
* **Gender Correction:** Implemented a dictionary-based validation to correct over 700 gender misclassifications based on first names.

## 🚀 Next Steps: Data Architecture Scalability
To transition this from a static analysis to a live product, the future architecture proposes:
1. **Automated Ingestion:** Replacing manual CSV uploads by building ETL pipelines with **n8n** and JavaScript to extract data directly from HR software.
2. **Cloud Storage:** Loading the processed data into **Google Cloud (BigQuery)** for centralized, secure access.
3. **BI Integration:** Connecting the data warehouse to **Power BI** for real-time dashboarding for the C-level.

---
*Created by Facundo Arnaudo - Analytics Engineer & Data Specialist*
