# Heart Disease Risk Prediction

A machine learning project comparing multiple classification models to predict heart disease risk from patient clinical data. Originally built as part of MSc coursework, refined here as a standalone project.

## Summary

This project predicts heart disease risk using the UCI Heart Disease dataset, roughly 918 patient records with 12 clinical features. Three classification models, Logistic Regression, Random Forest Classifier, and Support Vector Classifier, are trained and compared. Evaluation goes beyond accuracy alone, since in a medical risk context a false negative (missing a real case) is far more costly than a false positive.

## Tech stack

- Python
- scikit-learn
- pandas / NumPy
- matplotlib / seaborn for the correlation heatmap and ROC curve
- Plotly for interactive distribution and feature comparison plots
- Jupyter Notebook

## Models compared

- Logistic Regression
- Random Forest Classifier
- Support Vector Classifier

## Evaluation

Models are compared across multiple metrics rather than accuracy alone. In a medical risk context, false negatives matter more than raw accuracy.

| Model | Accuracy | Recall | F1 | MSE | MAE |
|---|---|---|---|---|---|
| Logistic Regression | 0.8424 | 0.9126 | 0.8664 | 0.1576 | 0.1576 |
| Random Forest Classifier | 0.8587 | 0.9223 | 0.8796 | 0.1413 | 0.1413 |
| Support Vector Classifier | 0.8478 | 0.9126 | 0.8704 | 0.1522 | 0.1522 |

Precision wasn't computed in the source notebook, so it isn't included here.

## Key findings

Random Forest performed best overall: highest accuracy at 85.87%, highest F1 at 0.8796, highest recall at 0.9223, and the lowest error (MSE/MAE of 0.1413) of the three. SVC came second at 84.78% accuracy, just ahead of Logistic Regression at 84.24%. All three models landed in a similar recall range, around 91-92%, which is what matters most here. In a heart disease screening context, missing a true positive case is far costlier than a false alarm.

## How to run

\`\`\`bash
git clone https://github.com/semilhalani/heartdiseaseprediction.git
cd heartdiseaseprediction
pip install -r requirements.txt
jupyter notebook Heart-Failure_Prediction.ipynb
\`\`\`
