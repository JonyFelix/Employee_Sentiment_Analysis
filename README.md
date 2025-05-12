# Employee_Sentiment_Analysis


## 📝 Project Overview

This project aims to evaluate employee sentiment based on their email communications and identify individuals who may be at risk of leaving the organization. Using natural language processing (NLP) and machine learning techniques, we extract insights from employee-written text to:
- Score sentiments of communications.
- Rank employees based on positivity or negativity.
- Predict potential flight risks.
- Build a regression model to predict sentiment scores using text features.

---

## 📂 Dataset

The dataset includes internal communications between employees in `.csv` format with the following key columns:
- `Employee` – Sender of the email.
- `Email_Text` – Body of the communication,with Subject.
- `Date` (optional) – Timestamp of communication.

---

## 🔧 Methodology

### 1. Data Loading & Cleaning
- Loaded the CSV file and renamed columns for clarity.
- Handled missing/null values in the text or employee fields.
- Cleaned textual data (removal of special characters, case normalization).

### 2. Exploratory Data Analysis (EDA)
- Plotted sentiment distribution histogram.
- Created word frequency plots (optional).
- Counted emails per employee to identify outliers.
- Visualized various EDA factors like Total No of sentiments, Top 10 Empolyees, senders, Monthly Trends and more.

### 3. Sentiment Scoring (Using VADER)
- Applied VADER Sentiment Analyzer to compute compound sentiment scores.
- Classified each email as `Positive`, `Neutral`, or `Negative`.
- Observed that the majority of communications were neutral or slightly positive.

### 4. Employee Ranking
- Grouped data by `Employee`.
- Calculated average sentiment, number of emails, and sentiment variance.
- Identified:
  - 🔝 Top 3 Positive Employees
  - 🔻 Bottom 3 Negative Employees

### 5. Flight Risk Identification
- Defined flight risk criteria:
  - Low average sentiment (e.g., < -0.3).
  - High consistency in negative tone.
- Flagged employees meeting criteria.

### 6. Predictive Modeling
- Used TF-IDF vectorization on email text.
- Applied RandomForestRegressor to predict sentiment scores.
- Model evaluated using:
  - Mean Squared Error (MSE)
  - R² Score
- Exported predictions and rankings to Excel.

### 7. Conclusion & Recommendations
- Summarized key findings.
- Highlighted at-risk employees and top performers.
- Suggested HR engagement with low-score individuals for retention.

---




