# 🚗 Car Evaluation with Machine Learning  

## 📌 Project Overview  
This project applies machine learning techniques to classify cars based on their attributes using the **Car Evaluation Dataset** from the [UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Car+Evaluation). The goal is to predict whether a car falls into one of four categories: **unacceptable, acceptable, good, or very good**.  

### 🔍 **Key Features**
- **Explores multiple ML models**: Decision Tree, k-NN, Logistic Regression, Naïve Bayes, and SVM.
- **Handles ordinal data**: One-Hot Encoding used to preserve categorical distinctions.
- **Imbalanced dataset solutions**: MCC included for robust performance tracking.
- **Nested Cross-Validation**: 5-fold stratified inner/outer loops to ensure reliable model selection.
- **Hyperparameter Tuning**: GridSearchCV applied for optimal parameter selection.
- **Evaluation Metrics**: Accuracy, MCC, Precision, Recall, F1-score, and ROC analysis.
- **Final Model Selection**: SVM demonstrated the highest classification performance.

---

## 📊 **Dataset Details**
- **Total records**: 1728  
- **Features**: 6 categorical attributes  
- **Target variable**: Categorical (4 classes)  
- **Classes**:  
  - `unacceptable` (unacc)  
  - `acceptable` (acc)  
  - `good` (good)  
  - `very good` (vgood)  

---

## 🏗 **Project Structure**
- `README.md` → Project documentation  
- `car-evaluation.ipynb` → Jupyter Notebook with code and analysis  
- `car-evaluation.pdf` → PDF version of the notebook  
- `car.data` , `car.names` → Raw dataset  

---

## 🚀 **Final Model - SVM Fine-Tuning**
**Best Hyperparameters:**  
{
  "C": 10,
  "kernel": "poly",
  "gamma": 0.1,
  "degree": 5,
  "coef0": 1.0
}

---

## 🚀 **Final Performance on Test Set**
| Class  | Precision | Recall | F1-score |
|--------|----------|--------|----------|
| acc    | 97.96%   | 100%   | 98.97%   |
| good   | 100%     | 100%   | 100%     |
| unacc  | 100%     | 100%   | 100%     |
| vgood  | 100%     | 87.5%  | 93.33%   |

- **Overall Accuracy**: 99.54%  
- **Matthews Correlation Coefficient (MCC)**: 0.9899  

---

## 📈 **ROC Curve Analysis**
- **AUC for all classes is near 1**, confirming strong separation ability.
- **"vgood" class has a slightly lower AUC (~0.95)** due to its lower representation.
- **SVM demonstrated the best ROC performance**, making it the most reliable classifier.
- **Each class exhibits smooth ROC curves**, indicating minimal misclassification.

---

## 📌 **Key Takeaways**
✅ **SVM is the most effective model** for this dataset.  
✅ **Nested cross-validation** ensures unbiased model evaluation.  
✅ **Hyperparameter tuning significantly improved SVM performance**.  
✅ **Feature encoding played a crucial role in model performance**.  
✅ **Minor misclassification in "vgood" suggests potential improvements with class balancing techniques**.  

