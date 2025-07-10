# Credit Card Fraud Detection 

## 🚀 Project Overview 
An advanced fraud detection system evaluating 7+ ML models and 3 sampling techniques on highly imbalanced transaction data (284K+ transactions).

## 🔍 Key Insights
- **Optimal Sampling**: Random Undersampling (RUS) prevented overfitting observed in SMOTE (Synthetic Minority Oversampling) / Random Oversampling (ROS)
- **Critical Finding**: Fraud peaks **11 hours after initial transaction** (40 cases/hour) and all fraudulent transaction amounts were less than 5000
- **Optimal Threshold**: 0.85 probability balances recall (92%) and precision (96%)

## 🏆 Best Performing Models (RUS)
| Model               | Precision | Recall | F1-Score | AUC  | Speed        |
|---------------------|-----------|--------|----------|------|-----------   |
| Logistic Regression | 0.96      | 0.92   | 0.94     | 0.99 | ⚡ Fastest  |
| Stacked Ensemble    | 0.99      | 0.90   | 0.94     | 0.98 | 🐢 Slowest  |

## 💡 Recommendation
1. **Choose Logistic Regression if**:
- You prioritize recall (catching more fraud)
- You need fast inference (real-time systems)
- You value model interpretability
2. **Choose Stacked Ensemble if**:
- You prioritize precision (fewer false alarms)
- You can tolerate slower prediction speed
- You want slightly better robustness

## 🛠️ Technical Implementation
### Data Preparation
- **Dataset**: [Kaggle Credit Card Fraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
  - 284,807 transactions (492 frauds → 0.17% imbalance)
  - 30 features (PCA-transformed for privacy)
- **Cleaning**: Removed duplicates (1,081 records)

### Modeling Approach
1. **Sampling Techniques**:
   - Random Undersampling (RUS)
   - Random Oversampling (ROS)
   - SMOTE (Synthetic Minority Oversampling)

2. **Algorithms Tested**:
    - Decision Tree
    - Logistic Regression
    - Random Forest
    - XGBoost
    - MLP
    - Isolation Forest
    - Stacked Ensemble Model (RF + XGBoost + Logistic Regression)

3. **Evaluation Metrics**:
    - Classification Reports
    - Confusion Metrics
    - Precision-Recall Curves
    - ROC-AUC Curves
    
## 💡 Business Impact
- Identified optimal tradeoff between fraud detection (recall) and false alarms (precision)
- Demonstrated Random Undersampling superiority in real-world imbalance scenarios
- Provided actionable threshold recommendations for financial institutions

## 🚀 How to Use
- Clone repository
- Install requirements: pip install -r requirements.txt
- Run Jupyter notebook

## 📌 Note: For dataset access, visit the Kaggle source page
