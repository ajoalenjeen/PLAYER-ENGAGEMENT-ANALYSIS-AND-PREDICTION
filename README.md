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

---

## 🔑 Key Findings

1. **SessionsPerWeek is the dominant predictor of engagement**, followed by AvgSessionDurationMinutes. *How often* and *how long* players engage is the single strongest signal of engagement level.

2. **AchievementsUnlocked and PlayerLevel are secondary drivers.** Progression metrics matter, but well below raw activity metrics.

3. **Demographics (Age, Gender, Location) have minimal predictive power** — retention efforts should focus on behavioral interventions, not demographic targeting.

4. **In-game purchases matter only marginally.** Counterintuitive given the assumption that purchasers should be more engaged — worth investigating further.

5. **Tree-based models (Random Forest, XGBoost) outperformed linear baselines** on this multi-class engagement task.


---

## 📈 Recommendations

1. **Track session frequency as the primary engagement health metric.** Flag players whose weekly session count drops below threshold for re-engagement.
2. **Use session duration as a secondary signal.** Short sessions + low frequency = early churn warning.
3. **Deprioritize demographic targeting** in favor of behavior-based segmentation.
4. **A/B test in-game purchase incentives** — the model suggests they may not be the most effective retention lever.

---

## 🛠️ Methods Used

- **Exploratory Data Analysis** — distributions, skewness/kurtosis analysis, categorical breakdowns
- **Feature Encoding** — categorical encoding for tree-based models
- **Correlation Analysis** — feature relationships with the engagement target
- **Classification Modeling** — Random Forest and XGBoost
- **Model Evaluation** — accuracy, classification report, ROC-AUC
- **Feature Importance Analysis** — identifying the behavioral drivers of engagement

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
