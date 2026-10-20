# EDA of Income, Employment and Education

> Exploratory Data Analysis on the UCI Adult Census Income dataset (32,561 records) to understand what is linked to earning above $50K.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge) ![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge) ![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1aLQl1oHVOxs62j26eYoKCuksT6TpdgnN?usp=sharing)

## 📊 Project Overview
**Purpose:** Understand how education, working hours, age and other factors relate to whether a person earns above or below $50K a year.

**Dataset:** UCI Adult Income - 32,561 rows, 15 columns | Target: `income` (<=50K / >50K)

## 🔧 Tools & Technologies
- Python, Pandas
- Matplotlib, Seaborn, Plotly
- Google Colab

## 🧹 Data Cleaning
- Missing values: Workclass (1,836), Occupation (1,843), Native-Country (583) marked as "?" -> filled with "Unknown"
- Duplicates: 24 rows removed (32,561 -> 32,537)
- Fixed country names: Columbia, Hong, Trinadad&Tobago, Holand-Netherlands
- Outliers checked with box plots

## 📈 Visualizations & Key Findings

### 1. Income Distribution - Imbalanced
<img width="1591" height="448" alt="income_distribution" src="https://github.com/user-attachments/assets/df8ef119-1868-4b0a-a04d-7adb31654b77" />


*Finding: 75.9% earn <=50K and 24.1% earn >50K.*

### 2. Education Shows the Clearest Link with Income
<img width="1014" height="609" alt="education_income" src="https://github.com/user-attachments/assets/1630576e-c1d7-438e-9d1e-ec5037035517" />


*Finding: 74% of Doctorate and 73% of Prof-school holders earn >50K, versus only 16% of HS-grads.*

### 3. Working Hours
<img width="686" height="470" alt="hours_vs_income" src="https://github.com/user-attachments/assets/c1fa1f5f-72b6-43c0-9d80-1a3f555745fa" />


*Finding: >50K earners work about 45 hrs/week vs about 39 hrs for <=50K.*

### 4. Correlation Between Numeric Variables
<img width="855" height="528" alt="correlation_heatmap" src="https://github.com/user-attachments/assets/adfe89aa-826d-4505-b29a-0612fee96ba2" />


*Finding: Correlations are weak. The highest is education_num vs hours_per_week (0.15). Capital gain/loss are 0 for most people.*

### 5. Gender Difference
<img width="686" height="470" alt="hours_by_sex" src="https://github.com/user-attachments/assets/db2f129e-944b-4d79-9f6b-5c83d8320992" />


*Finding: Men work more hours than women in both income groups.*

## 💡 Key Insights
- Only 24% of people earn >50K, so the data is imbalanced
- Education shows the clearest link with higher income
- >50K earners work about 6 more hours per week
- Median age is about 44 for >50K vs about 34 for <=50K

> Note: This is an exploratory analysis. It shows relationships (correlation), not cause and effect.

## ▶️ How to Run
1. Open the notebook in Google Colab using the badge above.
2. Upload `adult.data` to the Colab session.
3. Run all cells. To run locally: `pip install pandas matplotlib seaborn plotly`

## 📁 Repository Contents
- Jupyter / Colab notebook with the full analysis
- Project report
- `adult.data` - UCI Adult dataset
- 5 chart images (`.png`) used in this README

## 📚 Source
UCI Machine Learning Repository - Adult (Census Income) dataset.

