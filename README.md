## Report latex link: https://www.overleaf.com/read/gjzsgnbqrppt#100751
# EEG Seizure Prediction Using Logistic Regression

A comparative biomedical machine learning project for EEG seizure prediction across multiple EEG datasets using Logistic Regression, regularization techniques, PCA dimensionality reduction, and imbalance handling.

---

# Project Overview

This project investigates EEG seizure prediction using classical machine learning techniques across three different EEG datasets:

1. UCI Epileptic Seizure Recognition Dataset
2. CHB-MIT Clinical EEG Dataset
3. Bonn EEG Dataset

The project focuses on:

* EEG feature engineering
* Logistic Regression classification
* Regularization analysis
* PCA dimensionality reduction
* SMOTE imbalance handling
* Cross-dataset generalization
* Biomedical machine learning interpretation

The study demonstrates how dataset structure, feature redundancy, and signal representation influence seizure prediction performance.

---

# Datasets Used

## 1. UCI Epileptic Seizure Recognition

* Preprocessed tabular EEG dataset
* 178 EEG features
* Binary seizure classification
* Used for:

  * regularization analysis
  * PCA analysis
  * imbalance experiments

Dataset Source:
[https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition](https://archive.ics.uci.edu/ml/datasets/Epileptic+Seizure+Recognition)

---

## 2. CHB-MIT Clinical EEG

* Real multichannel clinical EEG recordings
* EDF EEG format
* 23 EEG channels
* 256 Hz sampling frequency
* Statistical EEG feature engineering

Dataset Source:
[https://physionet.org/content/chbmit/1.0.0/](https://physionet.org/content/chbmit/1.0.0/)

---

## 3. Bonn EEG Dataset

* Segmented EEG signals
* Binary seizure classification
* Compact EEG statistical representation
* Strong seizure separability

Dataset Source:
[https://epileptologie-bonn.de/cms/front_content.php?idcat=193&lang=3](https://epileptologie-bonn.de/cms/front_content.php?idcat=193&lang=3)

---

# Machine Learning Techniques

The following techniques were implemented:

## Baseline Model

* Logistic Regression

## Regularization

* L1 Regularization
* L2 Regularization
* Elastic Net Regularization

## Imbalance Handling

* SMOTE Oversampling
* Class Weighting

## Dimensionality Reduction

* PCA (Principal Component Analysis)

## Additional Analysis

* Learning Curves
* Underfitting vs Overfitting
* Cross-Dataset Comparison
* Sparsity Analysis

---

# Project Structure

```text
EEG-Seizure-Prediction/
│
├── notebooks/
│   ├── uci_experiments.ipynb
│   ├── chbmit_experiments.ipynb
│   ├── bonn_experiments.ipynb
│   └── final_analysis.ipynb
│
├── figures/
│   ├── cross_dataset_performance.png
│   ├── regularization_comparison.png
│   ├── prauc_comparison.png
│   ├── sparsity_comparison.png
│   ├── pca_reduction_comparison.png
│   ├── chbmit_eeg_signal.png
│   └── bonn_eeg_signal.png
│
├── results/
│   ├── uci_results.csv
│   ├── chbmit_results.csv
│   ├── bonn_results.csv
│   └── cross_dataset_summary.csv
│
├── report/
│   ├── ieee_report.tex
│   └── ieee_report.pdf
│
├── README.md
└── requirements.txt
```

---

# Key Results

## Cross-Dataset Baseline Performance

| Dataset               | Accuracy | F1 Score | PR-AUC |
| --------------------- | -------- | -------- | ------ |
| UCI Epileptic Seizure | 0.8161   | 0.1557   | 0.4307 |
| CHB-MIT Clinical EEG  | 0.9931   | 0.6667   | 0.6131 |
| Bonn EEG              | 0.9600   | 0.8947   | 0.9343 |

---

# Major Findings

## 1. Dataset Structure Strongly Influences Performance

Performance varied significantly across datasets:

* Bonn EEG achieved strongest seizure separability
* CHB-MIT generalized well despite severe imbalance
* UCI underperformed despite high dimensionality

---

## 2. Regularization Behavior Depends on Feature Redundancy

| Dataset  | L1 Sparsity |
| -------- | ----------- |
| UCI      | 21.91%      |
| CHB-MIT  | 89.57%      |
| Bonn EEG | 0%          |

This demonstrated:

* CHB-MIT contained highly redundant engineered EEG features
* Bonn EEG features were compact and informative

---

## 3. PCA Compression Varied Across Datasets

| Dataset  | Original Features | Reduced Features |
| -------- | ----------------- | ---------------- |
| UCI      | 178               | 39               |
| CHB-MIT  | 115               | 35               |
| Bonn EEG | 5                 | 3                |

---

## 4. SMOTE Effectiveness Was Dataset-Dependent

* UCI: Improved F1-score
* CHB-MIT: Limited improvement
* Bonn EEG: Improved PR-AUC

---

# Visualizations

## Cross-Dataset Performance

![Cross Dataset Performance](figures/cross_dataset_performance.png)

---

## Regularization Comparison

![Regularization Comparison](figures/regularization_comparison.png)

---

## PR-AUC Comparison

![PR-AUC Comparison](figures/prauc_comparison.png)

---

## Sparsity Comparison

![Sparsity Comparison](figures/sparsity_comparison.png)

---

## PCA Feature Reduction

![PCA Reduction](figures/pca_reduction_comparison.png)

---

# Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Seaborn
* MNE
* Imbalanced-learn
* Jupyter Notebook
* LaTeX

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/EEG-Seizure-Prediction.git
cd EEG-Seizure-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Running the Project

Run the notebooks sequentially:

1. UCI experiments
2. CHB-MIT experiments
3. Bonn EEG experiments
4. Final analysis and visualization notebook

---

# Future Improvements

Potential future work includes:

* Deep learning EEG classification
* CNN/LSTM seizure prediction
* Time-frequency EEG analysis
* Real-time seizure monitoring
* Explainable AI for EEG interpretation
* Patient-specific seizure prediction
* Transfer learning across EEG datasets

---

# Research Contribution

This project demonstrates that:

* Classical machine learning models remain highly effective for EEG seizure prediction.
* EEG feature representation strongly affects model generalization.
* Regularization and PCA effectiveness depend heavily on dataset structure.
* Biomedical machine learning pipelines require dataset-specific preprocessing strategies.

---

# Author

Kaleem Hussaini

Department of Data Science

Institute of Mangement Sciences Peshawar

---

# License

This project is for educational and research purposes.
