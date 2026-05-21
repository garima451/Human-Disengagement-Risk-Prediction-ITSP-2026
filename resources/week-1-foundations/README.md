# 🌱 Week 1 - Foundations

Welcome to Week 1 of the Human Disengagement Risk Prediction Project!

This week is focused on building the basic foundation required for the project.

Do NOT worry if you are completely new to machine learning, Python, GitHub, or data analysis.

The goal of this week is simply to become comfortable with:

- 😍 Google Colab
- 😍 Python basics
- 😍 pandas basics
- 😍 datasets
- 😍 basic visualizations

---

## 🎯 Week Goal

By the end of Week 1, every team member should be able to:

- 🤔 Open and use Google Colab
- 🤔 Run Python code
- 🤔 Understand rows and columns in datasets
- 🤔 Load CSV files using pandas
- 🤔 Perform basic dataset exploration
- 🤔 Create simple visualizations

---

## 📂 Task Submission

Task submission will be done through the Google Drive folder.

You have to upload your downloaded Google Colab notebook in the submission folder through the link 

## Notebook Naming Format

YourName_Week1_Task1.ipynb

## 🐼 Week 1 Task

### 1. Download Dataset

Download the Employee Attrition Dataset as a CSV file through this link: [Week-1_Task-1_Submission](https://drive.google.com/drive/folders/1pRpMYJwDQOTbsuJmCgZBVr6jBQAciF7u?usp=drive_link)

[Employee Attrition Dataset](https://www.kaggle.com/code/faressayah/ibm-hr-analytics-employee-attrition-performance?select=WA_Fn-UseC_-HR-Employee-Attrition.csv)

---

### 2. Upload Dataset on Google Colab

Upload this CSV file on Google Colab.

Get used to Google Colab through any online resource you are comfortable with.

---

### 3. Read Dataset Using pandas

Use pandas to read this file and store it as a DataFrame.

Understand what each line of code is doing.

### 4. Perform Dataset Preprocessing

Do complete dataset preprocessing.

This may include:

- checking missing values
- handling missing values
- encoding categorical features
- scaling numerical features
- removing irrelevant features
- correlation analysis
- multicollinearity analysis
- plotting final heatmap

## 🧩 Specific Things To Focus On

---

### A. Missing Value Handling

Check for missing values.

The general approach is replacing missing values using:

- mean
- median
- mode

But do not blindly apply these methods.

Think creatively.

For example:

- If a value is missing from a particular feature, what is the best way to fill it?
- Can another related feature help estimate the missing value?
- Can group-wise mean, median, or mode be better than using the whole column?
- Can department-wise, role-wise, or category-wise replacement make more sense?

Data science requires creativity.

So think, search, understand, and then apply.

---

### B. sklearn Preprocessing

Explore preprocessing tools from `sklearn`.

Some useful classes are:

- `StandardScaler()`
- `LabelEncoder()`
- `OneHotEncoder()`

These are used for:

- scaling numerical values
- converting categorical values into numerical values
- preparing data for machine learning models

Machine learning models work better with numbers.

Think carefully:

- Which feature should be encoded?
- Which feature should be scaled?
- Which method is suitable for each feature?
- Why are you applying that method?

---

### C. Feature Relevance

A major part of preprocessing is understanding which features are relevant.

Manually inspect the features and think:

- Does this feature make sense for predicting the target?
- Is this feature useful?
- Is this feature constant?
- Is this feature redundant?
- Should this feature be dropped?

You may also use correlation analysis between features and the target.

---

### D. Correlation Analysis

The main target of this week is to plot the final heatmap showing correlation between features and the target.

You should:

- calculate correlation between features
- calculate correlation with the target variable
- plot the final heatmap
- understand what the correlations mean
- calculate Pearson correlation coefficient
- understand positive, negative, and near-zero correlation

---

### E. Linearity and Non-Linearity

Try to understand whether the dataset behaves in a linear or non-linear way.

Think about:

- Do features show strong linear relationships?
- Are correlations weak but patterns still possible?
- Why can tree-based models handle non-linear patterns better?

---

### F. Multicollinearity

Check whether multicollinearity exists between independent features.

Understand:

- what multicollinearity means
- why it is bad
- why highly correlated independent features can create problems
- why one of the highly dependent features may need to be removed

Also explain the mathematical reason.

Think in terms of matrices:

- What happens when two rows or columns are linearly dependent?
- What problem arises in matrix operations?
- Why does redundancy reduce useful information?

---

## 📝 Colab Notebook Instructions

Use text cells to write your understanding.

Use code cells to write and execute code.

Use comments in code wherever needed.

