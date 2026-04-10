# PLAYER-ENGAGEMENT-ANALYSIS-AND-PREDICTION

### Predicting Online Gaming Engagement to Inform Retention Strategy

A machine learning project that analyzes online gaming behavior to predict player engagement levels and identify the behavioral signals that drive retention.

---

## 🎯 Project Goal

Predict player engagement levels (High / Medium / Low) using behavioral and demographic features, and identify which signals a gaming company could use to flag at-risk players early for targeted retention campaigns.

---

## 📈 Model Performance

| Model              | Accuracy | AUC    |
|-------------------|---------:|-------:|
| XGBoost           | **91.88%** | 0.9461 |
| Random Forest     | 91.48%   | 0.9441 |
| LightGBM          | 91.27%   | **0.9464** |


XGBoost outperformed Random Forest and LightGBM on this multi-class engagement prediction task. The top features driving predictions were SessionsPerWeek and AvgSessionDurationMinutes — confirming that *behavioral activity* signals dominate over demographic features.

## 🔑 Key Findings

1. **Session frequency and playtime are the strongest engagement predictors.** Feature importance analysis ranks behavioral metrics far above demographic features — how players *behave* matters more than who they *are*.

2. **In-game purchase behavior correlates strongly with engagement level.** Players who make in-game purchases are disproportionately concentrated in the high-engagement group, suggesting purchases are both a *signal* of engagement and a potential *driver*.

3. **Demographic features (age, gender, location) have minimal predictive power.** This is a useful negative finding — retention efforts should focus on behavioral interventions, not demographic targeting.

4. **Random Forest and XGBoost both achieve strong classification performance**, with tree-based models outperforming linear baselines on this multi-class engagement task.

---

## 🛠️ Methods Used

- **Exploratory Data Analysis** — distributions, skewness/kurtosis analysis, categorical breakdowns
- **Feature Encoding** — categorical encoding for tree-based models
- **Correlation Analysis** — feature relationships with the engagement target
- **Classification Modeling** — Random Forest and XGBoost
- **Model Evaluation** — accuracy, classification report, ROC-AUC
- **Feature Importance Analysis** — identifying the behavioral drivers of engagement

---

## 📈 Recommendations

Based on the model and feature importance analysis, a gaming company could:

1. **Flag low-engagement players in their first 1-2 weeks** based on session frequency thresholds, and target them with personalized re-engagement campaigns before churn occurs.
2. **Offer in-game purchase incentives** to medium-engagement players to nudge them toward the high-engagement segment.
3. **Deprioritize demographic-based targeting** in favor of behavior-based segmentation, since demographic features showed minimal predictive value.

---

## 📂 Repository Structure

```
player-engagement-analysis/
├── data/
│   └── raw/
├── notebooks/
│   └── player_engagement_analysis.ipynb
├── README.md
└── requirements.txt
```

---

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/ajoalenjeen/player-engagement-analysis.git
cd player-engagement-analysis

# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook notebooks/player_engagement_analysis.ipynb
```

---

## 🧰 Technologies

Python · pandas · NumPy · scikit-learn · XGBoost · matplotlib · seaborn · Jupyter

---

## 👤 Author

**Ajo Alenjeen**
MBA Candidate, Business Analytics — Pace University
[LinkedIn](https://www.linkedin.com/in/ajoalenjeen/) · [Portfolio](https://github.com/ajoalenjeen)
