Here is a **fully professional, publication-quality README** with formal tone, structured presentation, and a clean consolidated results table. You can directly use this in your repository.

---

# Intent–Behavior Deviation Detection in Smart Contracts

### A Multi-Tier Machine Learning and Deep Learning Framework

---

## 1. Introduction

Smart contracts deployed on blockchain platforms are immutable and autonomous, making security vulnerabilities particularly critical. One of the most damaging threats is the **rug pull**, where a contract behaves differently from its intended purpose.

This project proposes a **multi-tier analytical framework** for detecting such vulnerabilities by modeling the **deviation between declared intent and observed behavior** using a combination of classical machine learning and deep learning techniques.

---

## 2. Objective

The primary objectives of this work are:

* To construct a high-dimensional feature representation capturing both structural and behavioral characteristics of smart contracts
* To evaluate multiple modeling paradigms across increasing levels of complexity
* To compare performance across tiers using robust statistical validation
* To identify the most effective approach for real-world deployment scenarios

---

## 3. Methodology

### 3.1 Feature Engineering

* A **398-dimensional feature vector** is constructed per contract
* Features include:

  * Static code attributes
  * Behavioral indicators
  * Transactional and logical patterns
* Data preprocessing includes normalization and balancing strategies

---

### 3.2 Model Architecture

The system is divided into three tiers:

| Tier   | Model Type                 | Description                                      |
| ------ | -------------------------- | ------------------------------------------------ |
| Tier 1 | Classical Machine Learning | Logistic Regression, Random Forest, SVM, XGBoost |
| Tier 2 | Shallow Neural Network     | Multi-Layer Perceptron (3 layers)                |
| Tier 3 | Deep Neural Network        | Deep MLP (5 layers, regularized)                 |

---

### 3.3 Training Strategy

* **5-Fold Stratified Cross-Validation**
* Class imbalance handled using balanced dataset experiments
* Hyperparameter tuning applied to neural models
* Regularization techniques:

  * Dropout
  * Early stopping

---

## 4. Experimental Setup

* Task: Binary Classification

  * Class 0: Safe Contract
  * Class 1: Rug Pull
* Dataset size: ~665 samples after preprocessing
* Evaluation metrics:

  * F1 Score (primary metric)
  * ROC-AUC
  * Precision and Recall
  * Mean ± Standard Deviation across folds

---

## 5. Results

### 5.1 Combined Performance Comparison

| Model                  | Tier   | F1 Score (Full Dataset) | AUC (Full) | F1 Score (Balanced Dataset) | AUC (Balanced) |
| ---------------------- | ------ | ----------------------- | ---------- | --------------------------- | -------------- |
| Logistic Regression    | Tier 1 | 0.9676 ± 0.0087         | 0.9877     | 0.9667                      | 0.9928         |
| Random Forest          | Tier 1 | 0.9745 ± 0.0041         | 0.9961     | 0.9701                      | 0.9956         |
| Support Vector Machine | Tier 1 | 0.9698 ± 0.0045         | 0.9955     | 0.9682                      | 0.9950         |
| XGBoost                | Tier 1 | 0.9742 ± 0.0045         | 0.9960     | 0.9677                      | 0.9957         |
| MLP (3-Layer)          | Tier 2 | 0.9749 ± 0.0082         | 0.9912     | 0.9755                      | 0.9923         |
| Deep MLP (5-Layer)     | Tier 3 | 0.9748 ± 0.0058         | 0.9913     | 0.9760                      | 0.9919         |

---

### 5.2 Key Observations

* The **3-layer MLP (Tier 2)** achieves the highest overall F1 score on the full dataset
* The **5-layer Deep MLP (Tier 3)** achieves the best performance on the balanced dataset
* Classical models such as Random Forest and XGBoost remain highly competitive
* Performance variance across folds is low, indicating strong generalization

---

## 6. Discussion

The results demonstrate that:

* High-quality feature engineering significantly boosts performance even for classical models
* Deep learning provides incremental gains rather than drastic improvements
* Model complexity must be balanced with computational efficiency for deployment
* Ensemble-based classical methods remain strong baselines in structured data scenarios

---

## 7. Example Classification Performance

| Metric               | Value |
| -------------------- | ----- |
| Accuracy             | ~98%  |
| Precision (Rug Pull) | 0.98  |
| Recall (Rug Pull)    | 0.98  |
| F1 Score (Rug Pull)  | 0.98  |

---

## 8. Repository Structure

```
├── notebook-0-eda-487.ipynb         # Exploratory Data Analysis
├── notebook-1-tier1-classical.ipynb # Classical ML models
├── notebook-2-tier2-mlp.ipynb       # Shallow neural network
├── notebook-3-tier3-deep.ipynb      # Deep neural network
├── notebook-4-combined-results.ipynb# Final evaluation and visualization
├── tier1_raw_results.json
├── tier2_raw_results.json
├── tier3_raw_results.json
```

---

## 9. Limitations

* Dataset size is relatively small for deep learning models
* Feature engineering is domain-specific and may require adaptation for other blockchain ecosystems
* Real-time deployment considerations (latency, scalability) are not addressed

---

## 10. Future Work

* Integration with graph-based contract representations
* Exploration of transformer-based architectures
* Deployment in real-time blockchain monitoring systems
* Incorporation of explainable AI techniques

---

## 11. Conclusion

This work presents a structured and scalable approach to detecting rug pull vulnerabilities using a combination of machine learning and deep learning techniques. The findings indicate that while deep models offer slight improvements, well-engineered features allow classical models to achieve near-equivalent performance.

The framework is therefore suitable for practical deployment in blockchain security pipelines, offering both accuracy and efficiency.

---

## 12. Project Information

* Project Type: Capstone Project
* Duration: Summer 2025 – Spring 2026
* Final Defense: April 16, 2026

---

If you want, I can next:

* convert this into a **journal paper format (IEEE/ACM)**
* generate **architecture diagrams (publication quality)**
* or add **figures from your notebooks properly referenced inside the README**

