# Heart Disease Prediction Using Decision Tree Classifier

# Project Overview:
Heart disease is a significant health concern worldwide, primarily due to unhealthy lifestyle choices. Early detection is crucial, as it can lead to timely intervention and more effective treatment. This project leverages machine learning techniques to predict the presence of heart disease, allowing for quicker diagnosis and potentially improving patient outcomes.
In this study, we experiment with a heart disease dataset to explore various machine learning algorithms and build an optimized model, ultimately aiming to predict the likelihood of heart disease with high accuracy. Our analysis focuses on the Decision Tree classifier, with methods for model improvement, such as pruning and hyperparameter tuning.

# Dataset:
The dataset used for this project contains medical risk factors and patient information. Here are the main features:
- Age: Patient's age in years
- Gender: Patient's gender (0 = Male, 1 = Female)
- Chest Pain: Type of chest pain experienced (0–3)
- Resting Blood Pressure: Blood pressure level while resting (in mm/Hg)
- Cholesterol: Serum cholesterol level (in mg/dl)
- Fasting Blood Sugar: Blood sugar level after fasting (1 if > 120 mg/dl, otherwise 0)
- Rest ECG: Resting electrocardiographic results (0–2)
- Max Heart Rate: Maximum heart rate achieved
- Exercise-Induced Angina: Exercise-induced angina (1 = Yes, 0 = No)
- ST Depression: ST depression induced by exercise relative to rest
- Slope: Slope of the peak exercise ST segment (0–2)
- Major Vessels: Number of major vessels colored by fluoroscopy (0–4)
- Thalassemia: Thalassemia status (0–3)
- Target: Presence of heart disease (1 = Yes, 0 = No)

# Data Exploration and Preprocessing
## Exploratory Data Analysis
- Statistical Summary: We performed summary statistics on both numerical and categorical variables.
- Distribution Analysis: Checked for skewness and near-normal distributions among variables, finding slight skewness in some.
- Correlation Analysis: Low to moderate correlations were found, with no signs of multicollinearity.
- Data Cleaning and Outlier Treatment
- Outlier Detection and Handling: Identified outliers in features like rest_bps, cholestrol, thalach, and old_peak using boxplots. Outliers were removed to ensure the data was more normally distributed and improve model performance.

# Model Building
- Our analysis focused on the Decision Tree algorithm due to its interpretability and ability to handle both categorical and numerical data effectively.

## Baseline Model:
- Utilized unscaled features to build an initial Decision Tree with an accuracy of 71%.
- Plotted the ROC curve, showing an AUC score of 0.7105.

## Model Improvement:
- Pruning: Reduced tree complexity to prevent overfitting, increasing accuracy to 76% and achieving an AUC score of 0.7389.
- Hyperparameter Tuning: Employed GridSearchCV to find optimal parameters for our Decision Tree, yielding 79% accuracy with an AUC score of 0.7543.

## Performance Evaluation:
- Confusion Matrix: Visualized performance across all models to identify sensitivity and specificity.
- ROC Curve: Plotted ROC curves for each iteration, demonstrating significant improvements as we optimized the model.

## Results
- The optimized Decision Tree (with GridSearchCV) achieved the following performance metrics:

Accuracy: 79%
AUC Score: 0.7543
F1 Score: Higher compared to the baseline model
Recall and Precision: Improved with hyperparameter tuning and pruning

Based on these results, the Decision Tree model (with GridSearchCV) was the best-performing model and can be reliably used for early heart disease prediction.

# Future Work
- Ensemble Methods: Experiment with Random Forest and Gradient Boosting for potentially better performance.
- Model Generalization: Apply techniques such as cross-validation to improve model robustness.
- Larger Datasets: Expand the dataset to include more observations, enhancing model accuracy and generalizability.

## Conclusion
This project demonstrates that machine learning, particularly Decision Trees, can effectively aid in the prediction of heart disease. By refining the model through pruning and hyperparameter tuning, we achieved a significant improvement in accuracy and general performance. Early prediction models like this one are critical for proactive healthcare and can contribute meaningfully to the early diagnosis and treatment of heart disease.
