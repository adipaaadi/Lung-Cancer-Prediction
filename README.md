# Lung Cancer Prediction — ML Classification Study

Comparison of six classifiers on a 309-patient lung cancer symptom survey dataset, with a focus on class imbalance and metric selection.

## Key Findings

- **Accuracy was misleading.** All six models scored 86–89% accuracy, but the dataset is 87% positive / 13% negative. A model predicting "yes" for everyone would score ~84% without learning anything.
- **Macro-averaged F1 dropped to 0.71–0.75** across all models, revealing the true performance gap.
- **Logistic Regression and Random Forest** had the fewest false negatives (best for screening — missing a real case is worse than a false alarm).
- **Decision Tree** caught the most true negatives but missed 7 real cancer cases.
- **Feature scaling materially changed SVM behavior.** Before scaling, SVM was likely predicting the majority class; after scaling, it distinguished classes properly.

## Models Compared

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (RBF kernel)
- Naive Bayes
- Random Forest

## Dataset

`survey_lung_cancer.csv` — 309 patient records, 15 symptom/lifestyle features + 1 binary target (`LUNG_CANCER`).

## Stack

Python 3, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## Author

Adi Dasgupta — [LinkedIn](https://linkedin.com/in/adi-dasgupta-8737a2389)
