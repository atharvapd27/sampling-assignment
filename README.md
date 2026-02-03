# Evaluation of Sampling Techniques on Imbalanced Credit Card Data

**Course:** UCS654 – Predictive Analytics using Statistics  
**Assignment:** Assignment-2 (Sampling)  
**Author:** Atharva Pandey  
**Roll Number:** 102303372  

---

## Project Overview
This study focuses on the implementation and comparative analysis of various statistical sampling methods applied to a highly skewed credit card dataset. The goal is to measure how different sampling strategies impact the accuracy of machine learning classifiers, particularly in high-stakes scenarios like fraud detection where class imbalance is a significant challenge.

---

## Data Balancing Strategy
To mitigate the bias inherent in imbalanced data, I applied **Random Over Sampling** to create a perfectly balanced dataset before proceeding with the sampling experiments.

### Rationale for Over Sampling
* **Information Retention:** Unlike undersampling, this approach ensures no majority-class data is discarded.
* **Fair Training:** By equalizing class representation, the models can learn the features of the minority class (fraud) more effectively.
* **Stability:** A balanced foundation allows for a more consistent comparison between different sampling techniques.

---

## Methodology

### 1. Sampling Techniques
I extracted subsets from the balanced data using the following five statistical methods:
1. **Simple Random Sampling**
2. **Systematic Sampling**
3. **Stratified Sampling**
4. **Cluster Sampling**
5. **Bootstrap Sampling**

### 2. Machine Learning Classifiers
Each sample was evaluated across five distinct algorithms:
* **M1:** Gaussian Naive Bayes
* **M2:** Decision Tree
* **M3:** Random Forest
* **M4:** K-Nearest Neighbors (KNN)
* **M5:** Support Vector Machine (SVC)

---

## Comparative Results

### Accuracy Analysis (%)

| Sampling Method | Gaussian NB | Decision Tree | Random Forest | KNN | SVC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Simple Random** | 77.26 | 99.38 | 100.00 | 97.51 | 97.82 |
| **Systematic** | 80.79 | 98.25 | 100.00 | 96.51 | 96.94 |
| **Stratified** | 79.75 | 97.82 | 100.00 | 95.64 | 97.51 |
| **Cluster** | 100.00 | 99.07 | 100.00 | 92.52 | 97.20 |
| **Bootstrap** | 85.81 | 99.56 | 100.00 | 98.69 | 98.69 |

---

## Critical Observations

### Best Performers by Model
* **Gaussian Naive Bayes:** Optimized via **Cluster Sampling**.
* **Decision Tree:** Best results with **Bootstrap** or **Simple Random Sampling**.
* **Random Forest:** Displayed total stability with 100% accuracy across **all techniques**.
* **KNN & SVC:** Both reached peak performance using **Bootstrap Sampling**.

### Top Rankings
* **Ultimate Model:** **Random Forest** (Most robust and consistent).
* **Top Technique:** **Cluster Sampling** (Produced the highest overall gains for weaker models).

---

## Conclusion
The project underscores that effective class balancing is the cornerstone of handling imbalanced datasets. While **Random Forest** proved to be exceptionally resilient to sampling variations, the performance of other models varied significantly, highlighting the importance of selecting the right sampling-model pair. These results demonstrate that combining intelligent oversampling with robust ensemble algorithms leads to superior predictive performance in fraud detection tasks.
