# Breast Cancer Detection System

This project implements a breast cancer detection system using machine learning techniques. It explores three different classifiers—Decision Tree, Logistic Regression, and Random Forest—to classify patients as either having cancer (Malignant) or not having cancer (Benign), based on various input features.

# Project Overview
The dataset used is from the Breast Cancer Diagnostic Dataset, which contains features calculated from a digitized image of a fine needle aspirate (FNA) of a breast mass. These features describe the characteristics of the cell nuclei present in the image.

# Key Features:
## Classifiers Used:
• Decision Tree Classifier

• Logistic Regression Classifier

• Random Forest Classifier

## Metrics Evaluated:
• Accuracy

• F1 Score

• Precision

• Recall

• Confusion Matrix
## Visualization:
• Heatmap of feature correlations

• Countplots and pairplots for data visualization

• Kernel Density Estimation (KDE) plots for feature distributions

# Dataset
• Source: Breast Cancer Diagnostic Dataset

• Size: 569 samples, 33 features (including the target diagnosis)

• Target Variable: Diagnosis (M = Malignant, B = Benign)

# Features Used for Model Building:
The following features were used as input to the machine learning models:

• Radius_mean: Mean of distances from the center to points on the perimeter

• Texture_mean: Standard deviation of gray-scale values

• Perimeter_mean: Mean size of the core tumor

• Area_mean: Mean area of the tumor

• Smoothness_mean: Mean of local variation in radius lengths

• Compactness_mean: Mean of the perimeter^2 / area - 1.0

• Concavity_mean: Mean severity of concave portions of the contour

• Concave points_mean: Mean number of concave portions of the contour

• Symmetry_mean: Mean symmetry of the tumor

• Fractal dimension_mean: Mean "coastline approximation" of the tumor border

These features, among others, were crucial in predicting the likelihood of a tumor being malignant or benign.

## Libraries and Tools Used
• Python (3.9.12)

• Pandas

• NumPy

• Matplotlib

• Seaborn

• Scikit-learn


# How to Use

**1. Data Preprocessing:**

Load and explore the dataset, checking for null values and statistical properties.

Replace categorical target values ('M' = Malignant, 'B' = Benign) with numerical values (1 for M, 0 for B).

**2. Train-Test Split:**

The dataset is split into 80% training and 20% testing data using stratified sampling to maintain class balance.

**3. Models:**

• Decision Tree Classifier: This simple model fits the data with an accuracy of X%.

• Logistic Regression Classifier: Achieves an accuracy of Y% on the test set.

• Random Forest Classifier: The highest-performing model with an accuracy of Z%.

**4. Evaluation:**

• Metrics such as Accuracy, F1 Score, Precision, and Recall are calculated.

• Confusion matrix visualization is used to analyze the classification results.

**5. Results:**

![Screenshot 2024-09-29 112511](https://github.com/user-attachments/assets/89e567fd-51ea-4387-8a40-732eff0ce67f)

**For CNN:** 
Accuracy: 98.246%


**6. Prediction:**

The system can predict whether a patient has cancer based on input features. 

For example:

<pre>
<code class = "language-python">
patient = np.array([10.76, 24.54, 47.92, 181.0, 0.05263, 0.04362, 0.00000, 0.00000, 1.1587, 0.05884, 0.3857, 7.428, 2.548, 19.15, 0.007189, 0.00466, 0, 0, 0.02676, 0.002783, 9.456, 40.37, 59.16, 268.6, 0.08996, 1.06444, 0.0000, 1.0000, 0.2871, 4.07039])
prediction = classifier_rf.predict(patient.reshape(1, -1))
if prediction == 0:
    print('Patient has no cancer')
else:
    print('Patient has cancer')
</code>
</pre>


**7. Visualizations:**

• Correlation Heatmap: Displaying relationships between numerical features.

![output](https://github.com/user-attachments/assets/48fc0fdd-dc4f-4eda-8e5e-a9828425aa80)


• Countplot: Showing the distribution of malignant and benign cases.

![countplot](https://github.com/user-attachments/assets/564df0b7-e7da-4fe0-b4eb-6e90a4bbb553)


• Pairplot: Visualizing relationships between selected features for different diagnoses.

![output](https://github.com/user-attachments/assets/b34a29dc-79fd-4629-b0bc-a773c999324a)


• Confusion Matrix: Visualized for each classifier to show true positive/negative and false positive/negative predictions.

• Learning Curve for CNN:

![output1](https://github.com/user-attachments/assets/f787f119-00f0-48d6-9969-af9cc7967db1)
![output2](https://github.com/user-attachments/assets/d83ba0ef-bd7c-41a1-ae44-f451cf944ed3)

## Future Improvements

• Improve model performance with hyperparameter tuning.

• Experiment with additional machine learning models such as SVM or Neural Networks.

• Enhance the system with real-time prediction capabilities.
