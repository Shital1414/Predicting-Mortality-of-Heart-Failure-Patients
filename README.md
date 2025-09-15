# Heart Failure Mortality Prediction

[cite_start]This repository contains a machine learning project focused on predicting mortality in heart failure patients using clinical records data[cite: 254, 265]. [cite_start]The primary goal is to develop a predictive model that can serve as a clinical decision support tool, helping to identify high-risk patients for early intervention[cite: 265, 399]. [cite_start]This analysis was conducted by RAMGOPAL[cite: 257].

## 📋 Dataset

The analysis is based on a clinical records dataset with the following characteristics:
* [cite_start]**Total Patients**: 299 [cite: 270, 276]
* [cite_start]**Total Features**: 13 (comprising 7 numerical and 5 binary features) [cite: 270, 276, 296, 297]
* [cite_start]**Data Quality**: 100% complete with no missing values [cite: 276]

## ⚙️ Methodology

[cite_start]A logistic regression model was implemented to perform binary classification on the patient data[cite: 271, 327, 328]. The data processing and modeling pipeline involved the following steps:

1.  [cite_start]**Feature Scaling**: `StandardScaler` normalization was applied to all 7 numerical features to standardize their ranges[cite: 303, 316].
2.  [cite_start]**Train-Test Split**: The dataset was split into a training set (80% of the data, 239 samples) and a testing set (20% of the data, 60 samples)[cite: 310, 311, 317].
3.  [cite_start]**Model Training**: A logistic regression model was trained on the 239 samples to predict the mortality outcome (DEATH_EVENT: 0 or 1)[cite: 331, 332].

## 📈 Model Performance

The model's performance was evaluated on the test set of 60 samples, yielding the following results:

| Metric            | Score     |
| ----------------- | --------- |
| **Accuracy** | 81.67%    |
| **AUC Score** | 86.14%    |
| **Precision** | 78.57%    |
| **Recall (Sensitivity)** | 57.89%    |
| **F1-Score** | 66.67%    |
| **Specificity** | 92.7%     |

[cite_start]*Citations for the table values: Accuracy [cite: 333, 346][cite_start], AUC Score [cite: 341, 354][cite_start], Precision [cite: 335, 347][cite_start], Recall (Sensitivity) [cite: 337, 353, 383][cite_start], F1-Score [cite: 339, 352][cite_start], Specificity[cite: 384].*

### Confusion Matrix Analysis

The confusion matrix for the test set provides a detailed breakdown of the model's predictions:
* [cite_start]**True Positives**: 11 (Patients correctly predicted as deceased) [cite: 370]
* [cite_start]**True Negatives**: 38 (Patients correctly predicted as survivors) [cite: 368]
* [cite_start]**False Positives**: 3 (Patients incorrectly predicted as deceased) [cite: 369]
* [cite_start]**False Negatives**: 8 (Patients incorrectly predicted as survivors) [cite: 369]

## 📄 Conclusion

[cite_start]The logistic regression model demonstrates strong predictive capability with an overall accuracy of 81.67% and an excellent AUC score of 86.14%[cite: 387, 394].

* [cite_start]The model shows high specificity (92.7%), indicating it is very effective at correctly identifying patients who will survive[cite: 371, 384].
* [cite_start]The sensitivity (recall) is 57.9%, suggesting there is potential for improvement in correctly identifying all patients at risk of mortality[cite: 371, 383].

## 🚀 Future Directions

To further improve the model's performance and clinical applicability, the following steps are recommended:

* [cite_start]**Advanced Algorithms**: Explore more complex models such as ensemble methods, neural networks, or gradient boosting[cite: 390].
* [cite_start]**Feature Engineering**: Incorporate additional clinical markers and patient history data to enhance predictive power[cite: 392].
* [cite_start]**Clinical Validation**: Validate the model against larger, multi-center datasets to ensure its broader applicability[cite: 396].
* [cite_start]**Clinical Integration**: Develop a user-friendly interface to integrate the model into a real-time clinical decision support system[cite: 402].
