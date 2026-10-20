# EDA of Income, Employment and Education

> Exploratory Data Analysis on the UCI Adult Census Income dataset (32,561 records) to understand what is linked to earning above $50K.



![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)




![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)




![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)




![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)




![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)



[

![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)

](https://colab.research.google.com/drive/1aLQl1oHVOxs62j26eYoKCuksT6TpdgnN?usp=sharing)

### 📊 Project Overview
*Purpose:* Understand how education, working hours, age and other factors relate to whether a person earns above or below $50K a year.

*Dataset:* UCI Adult Income - 32,561 rows, 15 columns | Target: income (<=50K / >50K)

### 🔧 Tools & Technologies
- Python, Pandas
- Matplotlib, Seaborn, Plotly
- Google Colab

### 🧹 Data Cleaning
- Missing values: Workclass (1,836), Occupation (1,843), Native-Country (583) marked as "?" -> filled with "Unknown"
- Duplicates: 24 rows removed (32,561 -> 32,537)
- Fixed country names: Columbia, Hong, Trinadad&Tobago, Holand-Netherlands
- Outliers checked with box plots

### 📈 Visualizations & Key Findings

#### 1. Income Distribution - Imbalanced


![Income Distribution](images/income_distribution.png)



Finding: 75.9% earn <=50K and 24.1% earn >50K.

#### 2. Education Shows the Clearest Link with Income


![Education vs Income](images/education_income.png)



Finding: 74% of Doctorate and 73% of Prof-school holders earn >50K, versus only 16% of HS-grads.

#### 3. Working Hours


![Hours vs Income](images/hours_vs_income.png)



Finding: >50K earners work about 45 hrs/week vs about 39 hrs for <=50K.

#### 4. Correlation Between Numeric Variables


![Correlation Heatmap](images/correlation_heatmap.png)



Finding: Correlations are weak. The highest is education_num vs hours_per_week (0.15). Capital gain/loss are 0 for most people.

#### 5. Gender Difference


![Hours by Sex and Income](images/hours_by_sex.png)



Finding: Men work more hours than women in both income groups.

### 💡 Key Insights
- Only 24% of people earn >50K, so the data is imbalanced
- Education shows the clearest link with higher income
- >50K earners work about 6 more hours per week
- Median age is about 44 for >50K vs about 34 for <=50K

> Note: This is an exploratory analysis. It shows relationships (correlation), not cause and effect.

### ▶️ How to Run
1. Open the notebook in Google Colab using the badge above.
2. Upload adult.data to the Colab session.
3. Run all cells. To run locally: pip install pandas matplotlib seaborn plotly

### 📁 Repo Structure

├── EDA_Income_Employment_Education.ipynb   # Notebook
├── Project_Exploratory_Data_Analysis_...   # Project report
├── adult.data                              # UCI Adult dataset
├── images/                                 # Charts used in this README
└── README.md


### 📚 Source
UCI Machine Learning Repository - Adult (Census Income) dataset.
