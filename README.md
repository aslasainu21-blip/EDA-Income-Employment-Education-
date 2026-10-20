# EDA of Income, Employment and Education

> Exploratory Data Analysis on UCI Adult Census Income Dataset (32,561 records) to understand what drives income above $50K.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)

### 📊 Project Overview
**Purpose:** Understand how education, working hours, age and other factors relate to whether a person earns above or below $50K a year.

**Dataset:** UCI Adult Income - 32,561 rows, 15 columns | Target: `income` (<=50K / >50K)

### 🔧 Tools & Technologies
- Python, Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Google Colab

### 🧹 Data Cleaning
- Missing values: Workclass (1,836), Occupation (1,843), Native-Country (583) marked as "?" -> Filled as "Unknown"
- Duplicates: 24 rows removed (32,561 -> 32,537)
- Fixed Country names: Columbia, Hong, Trinadad&Tobago etc.

### 📈 Visualizations & Key Findings

#### 1. Income Distribution - Highly Imbalanced
Only 24% earn >50K.
![Income Dist](images/income_distribution.png)
*Finding: 75.9% <=50K, 24.1% >50K*

#### 2. Education is the Strongest Driver
![Education](images/education_income.png)
*Finding: 74% Doctorate & 73% Prof-school earn >50K vs only 16% of HS-grads.*

#### 3. Working Hours Matters
![Hours](images/hours_vs_income.png)
*Finding: >50K earners work ~45 hrs/week vs ~39 hrs for <=50K.*

#### 4. Correlation Between Numeric Variables
![Heatmap](images/correlation_heatmap.png)
*Finding: Weak correlations. Max is education_num vs hours_per_week (0.15). Capital gain/loss are 0 for most people.*

#### 5. Gender Gap
*Finding: Men work more hours than women in both income groups, leading to income gap.*

### 💡 Key Insights
- 24% of people earn >50K - Data is imbalanced
- Education shows clearest link with higher income
- +6 hours more per week for >50K earners
- Median age 44 for >50K vs 34 for <=50K

### 📁 Repo Structure
