# Telecom Customer Churn Prediction Pipeline 

##  Project Overview
Customer retention is significantly cheaper than acquisition. This project builds a predictive system to identify customers at high risk of churning (canceling service). The pipeline focuses on **Recall** to ensure the maximum number of potential churners are flagged for intervention strategies.

**[View the Project Analysis](./prediction_pipeline.ipynb)**

##  Key Challenges & Solutions
| Challenge | Solution |
|-----------|----------|
| **Class Imbalance** | Utilized **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the dataset. |
| **False Negatives** | Optimized model threshold to prioritize **Recall** over Precision. |
| **Explainability** | Chose Tree-based models (Random Forest/XGBoost) over Neural Networks to provide interpretable reasons for churn. |

##  Tech Stack
- **Language:** Python
- **Libraries:** Scikit-learn, Imbalanced-learn (SMOTE), Pandas, NumPy.
- **Models:** XGBoost, Random Forest.

##  Business Implications
The model serves as an "Early Warning System."
- **Action:** Customers flagged with >70% churn probability are routed to the specialized retention team.
- **Impact:** Even a small uplift in retention (e.g., 5%) can lead to significant revenue preservation for the telecom provider.

##  Deployment Strategy
As recommended in the pipeline analysis:
1.  **API:** Model logic wrapped in **Flask/FastAPI** for real-time scoring.
2.  **Monitoring:** Setup drift detection to retrain the model if customer behavior changes significantly over time.

##  Visuals
*(Upload a screenshot of your Confusion Matrix or ROC Curve here if available)*
