# 🌳 Week 1 Task 2 — Feature Analysis & Logistic Regression

Welcome to Week 2!

Now that you have understood:
- preprocessing
- correlations
- multicollinearity
- feature relationships

it is finally time to move towards our first Machine Learning model 🚀

This week is extremely important because this is where we transition from:

```text
Understanding Data
        ↓
Applying Machine Learning
```

---

# 🎯 Main Focus of This Week

This week mainly focuses on:

- 📊 Heatmap analysis
- 🧠 Multicollinearity understanding
- 📈 Feature ranking
- 🧩 Feature selection
- 🤖 Logistic Regression
- ✂️ Train-Test Split
- 📉 Evaluation Metrics
- 📚 Interpretation of Results

---

# 📊 Step 1 — Analyse The Heatmap

Use the final heatmap generated during preprocessing.

Analyse:

- which features strongly correlate with the target variable
- which features strongly correlate with each other
- which features appear redundant
- whether correlations are positive or negative

Try to understand:

- feature relationships
- feature redundancy
- multicollinearity
- possible patterns in employee attrition

---

# 🧠 Step 2 — Remove Multicollinear Features

Now identify highly correlated independent features.

Remove features that may create multicollinearity problems.

Understand:

- what multicollinearity means
- why it is harmful
- why redundant information creates instability
- how linearly dependent columns affect matrix operations

Think mathematically:

If two columns are linearly dependent:
- the matrix loses independence
- redundancy increases
- coefficient estimation becomes unstable

Write your understanding in text cells inside Google Colab.

---

# 📈 Step 3 — Rank Features

Now rank the features according to their importance.

Possible approaches:
- correlation with target
- statistical reasoning
- domain understanding
- feature importance techniques

Select the:

# ✅ Top 15 Most Important Features

from the Employee Attrition Dataset.

---

# 📝 Step 4 — Analyse Top 15 Features

For each selected feature:

- explain what the feature represents
- explain why it may affect employee attrition
- explain whether correlation appears positive or negative
- explain whether the feature appears important or weak

Write detailed analysis in text cells inside Google Colab.

---

# 🧩 Step 5 — Construct Refined DataFrame

Create a new dataframe consisting of:

- the selected top 15 features
- the target variable

Example:

```python
selected_features = [
    'Age',
    'MonthlyIncome',
    'OverTime'
]

new_df = df[selected_features]
```

---

# 🚀 Step 6 — Apply Logistic Regression

Now comes the most awaited moment...

Our first Machine Learning model:

# 🤖 Logistic Regression

Since Employee Attrition prediction is a classification problem, we will use Logistic Regression as our first classification model.

Apply Logistic Regression on the newly constructed dataframe.

---

# 🧠 Step 7 — Understand Logistic Regression

Do NOT blindly apply the model.

Understand:

- what Logistic Regression actually does
- why it is called "Regression"
- sigmoid function
- probabilities
- decision boundaries
- coefficients
- log-odds
- classification thresholds

Think deeply about:
- how the model makes decisions
- how probabilities are converted into classes
- why Logistic Regression assumes linear relationships

---

# 📄 PDF 1 — Mathematical Explanation of Logistic Regression

Prepare a **handwritten PDF** on Logistic Regression.

Your PDF should contain:

- mathematical explanation of Logistic Regression
- sigmoid function
- probability interpretation
- decision boundary
- coefficients
- loss function intuition
- diagrams wherever possible

## Requirements

- handwritten
- neat and clean
- properly structured
- minimum 2–3 pages

Upload this PDF to Google Drive.

---

# ⚙️ Step 8 — Understand Logistic Regression Parameters

Understand important Logistic Regression parameters such as:

- `penalty`
- `C`
- `solver`
- `max_iter`
- `random_state`

Think about:

- what each parameter controls
- why changing parameters changes model behavior
- which parameters you are using in your model
- why you selected those parameter values

Example:

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(
    max_iter=1000,
    random_state=42
)
```

---

# ✂️ Step 9 — Train-Test Split

Before training the model, understand:

## Why do we split data?

Understand:

- training data
- testing data
- generalization
- overfitting
- data leakage

Apply train-test split properly.

Example:

```python
from sklearn.model_selection import train_test_split

X = new_df.drop('Attrition', axis=1)
y = new_df['Attrition']

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

---

# 🤖 Step 10 — Train Logistic Regression Model

Train the Logistic Regression model.

Example:

```python
model.fit(X_train, y_train)
```

Make predictions:

```python
y_pred = model.predict(X_test)
```

---

# 📊 Step 11 — Model Evaluation

Now evaluate the model.

Understand:

- why evaluation is necessary
- why accuracy alone is insufficient
- how classification metrics work

---

# 📌 Evaluation Metrics To Analyse

You must analyse:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Classification Report

---

# 📈 Confusion Matrix

Plot the confusion matrix.

Understand:

- True Positive
- True Negative
- False Positive
- False Negative

Example:

```python
from sklearn.metrics import confusion_matrix

cm = confusion_matrix(y_test, y_pred)
```

Plot the confusion matrix properly using `seaborn`.

---

# 📄 PDF 2 — Evaluation Metrics Analysis

Prepare a **typed PDF** containing:

- explanation of every evaluation metric
- interpretation of results obtained
- confusion matrix analysis
- what each metric means for attrition prediction
- whether results indicate strong or weak performance

Include:

- plots
- screenshots
- observations

Upload this PDF to Google Drive.

---

# 🧠 Step 12 — Logistic Regression Result Analysis

Now analyse the overall behavior of Logistic Regression on this dataset.

Think deeply:

- Did Logistic Regression perform well?
- Why or why not?
- Did linearity assumptions limit performance?
- Was the dataset too non-linear?
- Did feature interactions affect results?
- Was class imbalance affecting results?
- Why might tree-based models work better?

Relate your explanation with:

- dataset nature
- model assumptions
- evaluation metrics
- final performance

---

# 📄 PDF 3 — Logistic Regression Behaviour Analysis

Prepare a separate **typed PDF** containing:

- complete interpretation of Logistic Regression results
- relation between dataset nature and model behavior
- relation between metrics and model quality
- why Logistic Regression worked well or failed
- strengths and limitations of the model for this dataset

This explanation should be analytical and thoughtful.

Upload this PDF to Google Drive.

---

# 📂 Final Deliverables

You must submit:

## 1. Google Colab Notebook

Containing:

- preprocessing
- feature analysis
- feature selection
- Logistic Regression implementation
- train-test split
- evaluation metrics
- plots
- observations
- explanations

---

## 2. PDF 1

Handwritten mathematical explanation of Logistic Regression.

---

## 3. PDF 2

Typed evaluation metrics analysis.

---

## 4. PDF 3

Typed Logistic Regression behaviour analysis.

---

# 📌 Important Instructions

- Use text cells for explanations
- Use code comments wherever needed
- Keep notebook neat and structured
- Explain reasoning behind every important step
- Do NOT blindly use code without understanding

---

# 🌟 Main Learning Target

The goal is NOT just applying Logistic Regression.

The goal is understanding:

- why models behave differently
- why evaluation matters
- why preprocessing changes outcomes
- why linear models struggle with non-linear data
- how machine learning connects mathematics with human behavior analysis
````
