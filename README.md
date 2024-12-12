# Classification-Model
This project explores the factors ### Summary of Model Results for Employee Attrition Prediction  

**Dataset Used:** HR dataset for employee attrition prediction  

This summary presents the results of various machine learning models and techniques applied to predict employee attrition, organized from individual model performances to ensemble methods and their optimizations.  

---

### **1. Individual Model Performance**  

- **Logistic Regression (LR):** Accuracy = **87.0%**  
- **Decision Tree (DT):** Accuracy = **77.0%**  
- **Random Forest (RF):** Accuracy = **85.0%**  
- **K-Nearest Neighbors (KNN):** Accuracy = **85.0%**  

---

### **2. Voting Classifier Results**  

#### **Hard Voting Classifier**  
- Accuracy = **86.0%**  

#### **Soft Voting Classifier**  
- Accuracy = **87.0%**  

**Weights Analysis for Voting Classifier:**  
Different combinations of weights were applied to evaluate their impact. Accuracy values remained consistent across most weight configurations.  

- **(1, 1, 1, 1):** Accuracy = **86.0%**  
- **(2, 1, 1, 1):** Accuracy = **87.0%** (Best performance among weighted combinations)  
- Other weight combinations yielded accuracies between **83.0% - 86.0%**.  

---

### **3. Bagging Classifier Results**  

Bagging classifiers were tested using various base estimators:  

- **Logistic Regression after Bagging:** Accuracy = **87.0%**  
- **Decision Tree after Bagging:** Accuracy = **86.0%**  
- **KNN after Bagging:** Accuracy = **85.0%**  

Best configuration for bagging using randomized search:  
- **Parameters:**  
  `{n_estimators: 200, max_samples: 0.5, max_features: 0.75, estimator: LogisticRegression(), bootstrap_features: False, bootstrap: False}`  
- **Score:** **86.9%**  

---

### **4. Random Forest Results**  

Optimized using randomized search for hyperparameters:  
- **Parameters:**  
  `{n_estimators: 150, max_samples: 0.5, max_features: 'sqrt', max_depth: 15, criterion: 'gini', bootstrap: True}`  
- **Score:** **85.5%**  

---

### **Key Observations**  

1. **Logistic Regression emerged as the best-performing individual model** with an accuracy of **87.0%**.  
2. **Soft Voting Classifier with weights (2, 1, 1, 1)** achieved the highest accuracy of **87.0%** among ensemble methods.  
3. **Bagging Logistic Regression** also performed well with an accuracy of **87.0%**, closely matching the best individual model.  
4. **Random Forest** achieved slightly lower accuracy (**85.5%**) but remains a strong choice due to its robustness and interpretability.  

--- 

This analysis demonstrates that ensemble methods, particularly **Soft Voting** and **Bagging**, provide a slight edge over standalone models for employee attrition prediction.influencing Employee Attrition through classification algorithms
