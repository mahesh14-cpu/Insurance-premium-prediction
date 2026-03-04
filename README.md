🏥 Insurance Premium Prediction

Machine Learning project to predict health insurance premiums using **Random Forest Regression**.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org)



 📊 Project Overview

Predicts insurance premiums based on individual characteristics with **66% accuracy** (R² score) and **13.23% error rate** (MAPE).

Dataset:** 1,000,000 records | **Model:** Random Forest | **Features:** 15


 🎯 Key Results

| Metric | Value |
|--------|-------|
| **R² Score** | 0.6622 |
| **RMSE** | $2,567.91 |
| **MAE** | $2,041.34 |
| **MAPE** | 13.23% |

Top 3 Important Features:**
1. Smoker Status (45%) - Increases premium by ~32%
2. Coverage Level (30%) - Gold vs Bronze: +$2-3K/year
3. BMI (4%) - Obese: +15-20% premium

---

 🚀 Quick Start

 Installation
```bash
git clone https://github.com/mahesh14-cpu/Insurance-premium-prediction.git
cd Insurance-premium-prediction
pip install pandas numpy scikit-learn matplotlib seaborn
```

 Run Project
```bash
python 1_data_loading.py           # Load data
python 3_data_preprocessing.py     # Preprocess
python 4_model_training.py         # Train model
python 7c_simple_test.py           # Test predictions
```

 Make Prediction
```python
from 7c_simple_test import predict_insurance_premium

premium = predict_insurance_premium(
    age=35, gender='male', bmi=28.5, children=2,
    smoker='no', region='northwest', 
    medical_history='none', family_medical_history='none',
    exercise_frequency='regular', occupation='professional',
    coverage_level='gold'
)

print(f"Premium: ${premium:,.2f}")  # Output: $13,769.77
```

---

 📁 Project Structure

```
├── 1_data_loading.py              # Data extraction
├── 2_data_exploration.py          # EDA
├── 3_data_preprocessing.py        # Feature engineering
├── 4_model_training.py            # Model training
├── 5_model_evaluation.py          # Evaluation
├── 7c_simple_test.py              # Predictions
├── best_model.pkl                 # Trained model
├── feature_importance.png         # Visualization
└── FINAL_PROJECT_REPORT.txt       # Full report
```

---

🔧 Features Used

**Original (11):** age, gender, bmi, children, smoker, region, medical_history, family_medical_history, exercise_frequency, occupation, coverage_level

**Engineered (4):** age_group, bmi_category, high_risk, family_size

---

 💡 Key Insights

- **Smokers** pay $4,336 more annually
- **Gold coverage** costs $2-3K more than Silver
- **Healthy BMI** saves $200-500/year
- **Age impact** is surprisingly low (only 5.7% increase from 25 to 60)

---

 📈 Visualizations

![Feature Importance](feature_importance.png)
*Top features driving premium predictions*

![Model Evaluation](model_evaluation.png)
*Actual vs Predicted analysis*

---

 👨‍💻 Author

**Mahesh** - [@mahesh14-cpu](https://github.com/mahesh14-cpu)




⭐ Star this repo if you found it helpful!**
