# Machine_Learning-Loan_approval_classification

## Project Summary  

This project was developed as part of the **KNIME Challenge**, where our group achieved [**second place**](https://www.linkedin.com/posts/rosaria_knime-student-challenge-ugcPost-7326141038211776512-L7Pr?utm_source=share&utm_medium=member_desktop&rcm=ACoAADW12AQBUz2uIpJd8md73AqcJxwZr1Uz6_A).   
  
The task focused on building a machine learning model to classify **loan applications** as *risky* or *non-risky*, a typical problem in credit risk assessment.  

- **Dataset**:  
  - 252,000 rows and 11 variables describing applicants (economic, job-related, and socio-demographic features).  
  - After removing duplicates and redundant entries, the dataset was reduced to ~43,000 unique instances.  

- **Preprocessing**:  
  - Removal of duplicate rows and inconsistent city/state names.  
  - Feature encoding: binary encoding, ordinal encoding, and **target encoding** for high-cardinality variables (city, state, profession).  
  - Normalization applied to all features to ensure comparability and avoid bias.  

- **Handling Class Imbalance**:  
  - The dataset was highly imbalanced, with far fewer risky loans than safe ones.  
  - Applied different strategies: **holdout split with stratification**, **undersampling** of the majority class, and **oversampling with SMOTE** to generate synthetic risky-loan examples.  

- **Models**:  
  - Tested different families of models in KNIME/Weka:  
    - **Logistic Regression** (linear model)  
    - **Random Forest** (ensemble method)  
    - **Naive Bayes** (probabilistic model)  
    - **K-Nearest Neighbors (KNN)** (instance-based learning)  

- **Optimization**:  
  - Performed **systematic parameter tuning** with **Latin Hypercube Sampling (LHS)** and 10-fold cross-validation.  
  - Used the **F2-score** during tuning to prioritize **recall** (reducing false negatives, i.e., undetected risky loans).  

- **Evaluation**:  
  - Models were compared using **F1-score** (balancing precision and recall) and **ROC-AUC** (discriminative ability).  
  - The **best performing model** was **KNN (k=13) with SMOTE oversampling**.  
  - Final ROC-AUC achieved: **0.517**, highlighting the difficulty of the task but showing robustness in identifying risky loans compared to simpler baselines.  

- **Goal**: Develop a reliable approach to classify risky loans, minimizing false negatives, and contribute insights into credit risk modeling under class imbalance.  

---
