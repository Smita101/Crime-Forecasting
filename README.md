# Crime Category Forecasting

## Overview
This project tackles the **Crime Category Prediction Challenge**, aiming to forecast crime categories using machine learning models. By leveraging historical crime data, the project seeks to provide actionable insights for law enforcement agencies to allocate resources effectively and enhance public safety.

## Dataset Description
The dataset includes detailed information about criminal activities, such as:
- **train.csv**: Training dataset containing 20,000 records with 22 columns, including the target variable `crime_category`.
- **test.csv**: Test dataset with 5,000 records and 21 columns, excluding the target variable.
- **sample_submission.csv**: A sample submission file for competition.

### Features in the Dataset
- **Location & Coordinates:** Street address, cross streets, latitude, and longitude.
- **Dates & Time:** Date and time the crime was reported and occurred.
- **Crime Details:** Area name, reporting district, modus operandi, and weapon used.
- **Victim Demographics:** Age, gender, and descent of the victim.
- **Other Attributes:** Premise code and description, status, and crime category.

## Key Steps in the Project
### 1. Data Preprocessing
- Handled missing values using appropriate imputation techniques.
- Encoded categorical variables using methods like label encoding and ordinal encoding.
- Scaled numerical features using standardization for optimal model performance.

### 2. Exploratory Data Analysis (EDA)
- Visualized crime distribution by area, time, and victim demographics using Matplotlib and Seaborn.
- Highlighted significant trends and patterns in criminal activities.

### 3. Feature Engineering
- Extracted meaningful features from the dataset, including time-based variables and location data.
- Addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).

### 4. Model Building
- Experimented with multiple machine learning models:
  - Logistic Regression
  - Random Forest
  - XGBoost
  - LightGBM
  - Stacking Classifier
- Performed hyperparameter tuning using GridSearchCV and RandomizedSearchCV.

### 5. Model Evaluation
- Evaluated models using accuracy, precision, recall, F1-score, and ROC-AUC.

## Results
### Insights into Model Performances

1. **Logistic Regression Classifier**:
   - **Accuracy**: Validation accuracy of 0.65325 and test accuracy of 0.6728.
   - **Precision**: 0.6034
   - **Recall**: 0.6532
   - **F1 Score**: 0.5891
   - **Insight**: Balanced performance but struggles with precision and F1 score.

2. **Logistic Regression with Polynomial Features**:
   - **Accuracy**: Validation accuracy of 0.74775, test accuracy of 0.6756.
   - **Precision**: 0.7393
   - **Recall**: 0.7482
   - **F1 Score**: 0.7265
   - **Insight**: Improved validation performance but potential overfitting.

3. **KNN Classifier**:
   - **Accuracy**: Validation accuracy of 0.49725, test accuracy of 0.6728.
   - **Precision**: 0.7602
   - **Recall**: 0.4973
   - **F1 Score**: 0.5480
   - **Insight**: Conservative predictions with low recall.

4. **SVM**:
   - **Accuracy**: Validation accuracy of 0.5285, test accuracy of 0.6728.
   - **Precision**: 0.5359
   - **Recall**: 0.5285
   - **F1 Score**: 0.4458
   - **Insight**: Struggles with the dataset.

5. **Random Forest Classifier**:
   - **Accuracy**: Validation accuracy of 0.84825, test accuracy of 0.8462.
   - **Precision**: 0.8514
   - **Recall**: 0.8482
   - **F1 Score**: 0.8368
   - **Insight**: Strong performance with high metrics.

6. **LGBM Classifier**:
   - **Accuracy**: Validation accuracy of 0.85825, test accuracy of 0.8654.
   - **Precision**: 0.8759
   - **Recall**: 0.8582
   - **F1 Score**: 0.8566
   - **Insight**: Excellent metrics with high precision and F1 score.

7. **XGBoost Classifier**:
   - **Accuracy**: Validation accuracy of 0.86125, test accuracy of 0.8668.
   - **Precision**: 0.8774
   - **Recall**: 0.8612
   - **F1 Score**: 0.8600
   - **Insight**: Best-performing model with balanced metrics.

8. **Stacking Classifier**:
   - **Accuracy**: Validation accuracy of 0.85775, test accuracy of 0.8562.
   - **Precision**: 0.8722
   - **Recall**: 0.8602
   - **F1 Score**: 0.8578
   - **Insight**: Competitive performance similar to XGBoost and LightGBM.

9. **LGBM with SMOTE (Oversampling)**:
   - **Accuracy**: Validation accuracy of 0.86, test accuracy of 0.862.
   - **Precision**: 0.8803
   - **Recall**: 0.8600
   - **F1 Score**: 0.8586
   - **Insight**: Slight improvement with class imbalance handling.

### Conclusion
The XGBoost Classifier emerges as the best-performing model based on test accuracy and overall balanced performance across precision, recall, and F1 score. Models like LightGBM and Random Forest also perform very well, showing the effectiveness of ensemble methods. SMOTE further refines performance when addressing class imbalance.

## Installation and Usage
### Prerequisites
- Python 3.x
- Required libraries listed in `requirements.txt`.

### Steps to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/SmitaDhadhal/Crime-Forecasting.git
   ```
2. Navigate to the repository directory:
   ```bash
   cd Crime-Forecasting
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Jupyter Notebook:
   ```bash
   jupyter notebook Crime_Forecasting.ipynb
   ```

## Future Scope
- Explore advanced deep learning techniques for crime forecasting.
- Incorporate external datasets (e.g., weather or socioeconomic data) to improve predictions.

## Author
**Smita Dhadhal**  
- [GitHub Profile](https://github.com/SmitaDhadhal)  
- [LinkedIn](https://www.linkedin.com/in/smitadhadhal)



