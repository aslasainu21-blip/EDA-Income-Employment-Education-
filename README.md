# Exploratory Data Analysis of Income, Employment and Education

**Dataset:** UCI Adult Income (1994 U.S. Census)  
**Author:** Suvaibathul Aslamiya Up  
**Course:** AI-Driven Data Analytics  
**Tools:** Python | Pandas | NumPy | Matplotlib | Seaborn | Plotly | Google Colab

---

## 📌 Abstract
This project presents an Exploratory Data Analysis (EDA) of the UCI Adult Income dataset (1994 U.S. Census). The aim is to understand how educational, employment-related and demographic factors are associated with whether a person earns more than 50K per year.

**Key Stats:** 75.91% earn <=50K and 24.09% earn >50K. Higher education levels (Bachelors, Masters, Doctorate, Prof-school) are more strongly represented in the >50K group.

## 🎯 Project Objectives
- To analyze the relationship between education and income levels
- To examine how employment-related factors (workclass, occupation, working hours) are associated with income
- To study the influence of demographic factors (age, marital status, sex, race) on income
- To clean and preprocess data by handling missing values, removing duplicates, and checking outliers
- To summarize key findings using statistical analysis and visualizations

## 📂 Dataset Description

| Attribute | Value |
| :--- | :--- |
| Source | UCI Machine Learning Repository |
| Records | 32,561 individuals (32,537 after removing duplicates) |
| Features | 14 input features |
| Total columns | 15 (including target) |
| Target variable | Income (<=50K / >50K) |
| Data types | 6 numerical and 9 categorical columns |

**Column Groups:**
- **Demographic:** age, race, sex, native_country
- **Employment:** workclass, occupation, hours_per_week
- **Education:** education, education_num
- **Personal:** marital_status, relationship
- **Financial:** fnlwgt, capital_gain, capital_loss
- **Target:** income

## 🛠️ Tools and Technologies Used
- **Python (Google Colab):** programming and notebook environment
- **Pandas:** loading, cleaning, analyzing data
- **NumPy:** numerical operations
- **Matplotlib:** creating charts and graphs
- **Plotly:** interactive donut chart of income distribution
- **Seaborn:** count plots, box plots, heatmaps and pair plots



## 🧹 Data Cleaning and Preprocessing
- Missing "?" values were replaced with "Unknown"
- 24 duplicate records were removed
- Invalid and inconsistent values were checked and corrected
- Final dataset: 32,537 records

## 📊 Outlier Detection
Outliers detected using IQR method (Q1 - 1.5*IQR and Q3 + 1.5*IQR)
- Age: 142 potential outliers
- hours_per_week: 9,002
- capital_gain: 2,712
- capital_loss: 1,519

> These were retained because extreme values can be genuine observations (e.g., very high capital gains or long working hours).

## 🔍 Exploratory Data Analysis (EDA)

### Univariate Analysis
**Numerical:** age is slightly right-skewed (20-50 years), fnlwgt is strongly right-skewed, education_num peaks at 9, 10 and 13-14, capital_gain/capital_loss are zero for >90% records, hours_per_week peaks at 40 hours.

**Categorical:** Most work in Private sector, are Married-civ-spouse or Never-married, are White and Male, most belong to <=50K group. HS-grad and Bachelors are most frequent.

### Bivariate Analysis
- **Numerical vs Numerical:** age and hours_per_week show no strong linear relationship
- **Categorical vs Numerical:** >50K group has higher median age and higher average weekly hours
- **Categorical vs Categorical:** Education and income are clearly related

| Education | <=50K | >50K |
| :--- | :--- | :--- |
| Bachelors | 3,132 | 2,221 |
| Masters | 763 | 959 |
| Doctorate | 107 | 306 |
| Prof-school | 153 | 423 |
| HS-grad | 8,820 | 1,674 |
| Some-college | 5,896 | 1,386 |

### Statistical Analysis
| Variable | Mean | Median | Mode | Std. Dev. |
| :--- | :--- | :--- | :--- | :--- |
| age | 38.59 | 37 | 36 | 13.64 |
| fnlwgt | 189,780.85 | 178,356 | 123,011 | 105,556.47 |
| education_num | 10.08 | 10 | 9 | 2.57 |
| capital_gain | 1,078.44 | 0 | 0 | 7,387.96 |
| capital_loss | 87.37 | 0 | 0 | 403.10 |
| hours_per_week | 40.44 | 40 | 40 | 12.35 |

Strongest correlation: education_num and hours_per_week (0.148)

## 📈 Data Visualization and Interpretation

### Figure 1: Income category distribution (bar plot)
<img width="713" height="470" alt="download (2)" src="https://github.com/user-attachments/assets/599c6ac0-6069-4a58-a894-ebb04a6550b7" />

**Interpretation:** The data is imbalanced, with far more individuals in the <=50K group.

### Figure 2: Income category distribution (donut chart, Plotly)
<img width="439" height="172" alt="Screenshot 2026-10-20 153515" src="https://github.com/user-attachments/assets/183235d0-5339-443a-b244-65c2fc4414ad" />

**Interpretation:** 75.91% earn <=50K and 24.09% earn >50K.

### Figure 3: Histograms of numerical variables
<img width="1186" height="1190" alt="download (11)" src="https://github.com/user-attachments/assets/0b14b088-58e9-4083-bb4b-dbda6494f229" />

**Interpretation:** Most variables are skewed. capital_gain and capital_loss are concentrated at zero; hours_per_week peaks at 40.

### Figure 4: Box plots of numerical variables (plotted separately)
<img width="1189" height="1190" alt="download (10)" src="https://github.com/user-attachments/assets/f23be1ff-4377-4c88-b25a-8cb280bd042d" />

**Interpretation:** capital_gain, capital_loss, fnlwgt and hours_per_week show many extreme values; age and education_num are more balanced. Each variable is plotted separately because the scales differ.

### Figure 5: Count plots of categorical variables
<img width="1789" height="1390" alt="download (1)" src="https://github.com/user-attachments/assets/0fff29df-ef21-482e-9c2f-3088377b1b69" />

**Interpretation:** Private workclass, Married-civ-spouse and Never-married status, Husband and Not-in-family relationships, White race and Male sex are the largest groups.

### Figure 6: Age vs hours per week (scatter plot)
<img width="695" height="470" alt="download (3)" src="https://github.com/user-attachments/assets/88f8119b-d51e-436e-abc1-55b6afca1168" />

**Interpretation:** Points are widely scattered, so there is no strong linear relationship.

### Figure 7: Age distribution by income (box plot)
<img width="686" height="470" alt="download (4)" src="https://github.com/user-attachments/assets/7340564a-98df-4670-b302-30f1273db30e" />

**Interpretation:** The >50K group has a higher median age than the <=50K group.

### Figure 8: Average working hours by income (bar plot)
<img width="686" height="470" alt="download (5)" src="https://github.com/user-attachments/assets/af0cd613-1a56-4cd4-bf1e-817a0108fc49" />

**Interpretation:** The >50K group works slightly more hours per week on average.

### Figure 9: Average hours by sex and income (grouped bar plot)
<img width="686" height="470" alt="download (8)" src="https://github.com/user-attachments/assets/7a3f1c95-26f2-4c92-869e-711f413ec01e" />

**Interpretation:** The >50K group works longer hours for both sexes, with a bigger gap among males.

### Figure 10: Education level by income (count plot)
<img width="1014" height="609" alt="download (6)" src="https://github.com/user-attachments/assets/c1a643e4-3b12-44ab-850b-00596626b31d" />

**Interpretation:** Bachelors, Masters, Doctorate and Prof-school have a much larger share in the >50K group.

### Figure 11: Correlation heatmap of numerical variables
<img width="855" height="528" alt="download (7)" src="https://github.com/user-attachments/assets/95815ce5-12bd-4183-864a-aa5815f301fd" />

**Interpretation:** All correlations are weak; the highest is 0.15 between education_num and hours_per_week.

### Figure 12: Pair plot of numerical variables
<img width="1476" height="1528" alt="download (9)" src="https://github.com/user-attachments/assets/2001fa9e-5f58-44c7-88a4-c8936f41aace" />

**Interpretation:** No strong linear relationships are visible; capital_gain and capital_loss cluster around zero.

## 📈 Key Findings and Insights
- **Income distribution:** 75.91% earn <=50K and 24.09% earn >50K (imbalanced data)
- **Education:** Higher education is more represented in >50K group (Strongest effect)
- **Age:** >50K group has higher median age (Moderate effect)
- **Working hours:** >50K group works more hours per week on average (Moderate effect)
- **Sex and income:** >50K group works longer hours for both sexes, with bigger gap among males
- **Correlation:** All numerical correlations are weak (highest 0.15)

## ✅ Conclusion
Education level, age and working hours show clear patterns related to income category, with higher education being the most visible. However, these are associations only; findings do not establish causation.

## ⚠️ Limitations and Future Scope

**Limitations:**
- Data from 1994 U.S. Census, may not reflect current patterns
- Income has only two categories and data is imbalanced (76% vs 24%)
- capital_gain and capital_loss are mostly zero and highly skewed
- Outliers were retained, which can affect averages
- Analysis is exploratory, shows association not causation

**Future Scope:**
- Apply log transformation to skewed variables
- Build classification models (logistic regression, decision trees) with class imbalance handling
- Use statistical tests like chi-square test
- Use more recent data and add extra features

## 📚 References
- UCI ML Repository: Adult Dataset - https://archive.ics.uci.edu/dataset/2/adult
- Pandas, NumPy, Matplotlib, Seaborn documentation

---
