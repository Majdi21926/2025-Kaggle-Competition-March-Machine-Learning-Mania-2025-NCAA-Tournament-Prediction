#﻿**🏀 March Machine Learning Mania 2025 – NCAA Tournament Prediction**

**📌 Overview**

This project is my submission for Kaggle's **March Machine Learning Mania 2025** competition. The goal is to predict the probability that one NCAA basketball team will beat another in the tournament, using historical data and advanced machine learning techniques.

**🛠️ Project Workflow**

**1️. Data Exploration**

- The dataset consists of **35 CSV files**, including detailed and compact results of regular seasons and tournaments, team seeds, and sample submission files.
- Key datasets used:
  - **Regular Season Detailed Results** (Men & Women)
  - **NCAA Tournament Detailed Results** (Men & Women)
  - **NCAA Tournament Seeds**

**2️. Feature Engineering**

We engineered meaningful features to improve model predictions, including:

- **SeedNumDiff**: Difference in tournament seed numbers between teams.
- **WinRateDiff**: Difference in win rates between teams.
- **AvgPointDifferentialDiff**: Difference in average point differential.
- **AvgPointsScoredDiff & AvgPointsAllowedDiff**: Differences in offensive & defensive performance.
- **EloRatingDiff**: Difference in team Elo ratings.
- **TourneyWinPctDiff**: Difference in past tournament win percentages.

**3️. Feature Importance Analysis**

We analyzed feature importance using **permutation importance** to identify the most influential features:

- **EloRatingDiff** and **SeedNumDiff** emerged as the most important predictors.

**4️. Model Training & Evaluation**

**Approach 1: Baseline Models**

- **Logistic Regression**
  - **Brier Score:** 0.2498
  - **ROC AUC Score:** 0.5355
- **Random Forest**
  - **Brier Score:** 0.2088
  - **ROC AUC Score:** 0.7386
- **XGBoost Classifier**
  - **Brier Score:** 0.1813
  - **ROC AUC Score:** 0.8024

**Approach 2: Fine-Tuning XGBoost**

- **Hyperparameter tuning** was applied to optimize XGBoost.
- Achieved:
  - **Brier Score:** 0.3304
  - **ROC AUC Score:** 0.7313

**Approach 3: Fine-Tuning RandomForest (Best Model)**

- **Hyperparameter tuning** was applied to optimize RandomForest.
- Achieved**:**
  - **Brier Score:** 0.2098
  - **ROC AUC Score:** 0.8763

**5️. Final Submission Preparation**

- Used the **SampleSubmissionStage2.csv** to prepare matchups.
- Applied the best trained model to predict win probabilities.
- Ensured submission format matches Kaggle’s requirements (ID format: 2025\_TeamA\_TeamB).
-----
**📈 Key Learnings & Challenges**

✅ Importance of feature engineering in sports analytics.
✅ Season feature was problematic for predictions.
✅ Classification models vs. probability-based submissions.

**🚀 Next Steps**

- Try **LightGBM & CatBoost** for comparison.
- Experiment with **deep learning approaches**.
- Improve **generalization** to avoid overfitting.
-----
**🏆 Conclusion**

By focusing on **feature engineering, feature selection, and model optimization**, I significantly improved my prediction accuracy. This project highlights how **data-driven insights** can be used in **sports analytics & tournament predictions**.

📂 **Full Code & Notebooks available in this repo!** 🔥

