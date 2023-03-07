# Cardiovascular-Risk-Prediction

![tenor](https://user-images.githubusercontent.com/113933243/223390853-749b6a78-019c-4aa6-9f5b-c59b92c9d91c.gif)

# Problem Statement

The majority of people are not really aware of their unhealthy lifestyle, which can lead them to multiple serious diseases. One of them is coronary heart disease (CHD). Coronary heart disease is the term that describes what happens when your heart's blood supply is blocked or interrupted by a build-up of fatty substances in the coronary arteries.


In this project, I made a machine learning model that can predict after ten years whether the patient will have CHD or not with the best accuracy. I have the dataset from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts.


The classification goal is to predict whether the patient has a ten-year risk of future coronary heart disease (CHD). The dataset provides the patient's information. It includes 3390 records with 17 attributes. Each attribute is a potential risk factor. There are both demographic, and medical risk factors.

# Attribute Information

**id :-** unique identification of the patients.

**age :-** Patient age.

**education :-** Education of the patients.

**sex :-** Gender.

**is_smoking :-** Whether the patient is currently smoking or not.

**cigsPerDay :-** Cigrattes smoked per day.

**BPMeds :-** Whether taking BP meds or not.

**prevelantStroke :-** If the patient has a history of stroke.

**prevalentHyp :-** If the patient has a history of hypertension.

**diabetes :-** Patient has diabetes or not.
 
**totChol :-** Total cholesterol measure.

**sysBP :-** BP measure.

**diaBP :-** BP measure.

**BMI :-** Body mass index.

**heartRate :-** Heart rate measure.

**glucose :-** Blood glucose or blood sugar level in miligram per decilitere.

**TenYearCHD :-** After ten years the patient will have the coronary heart disease or not.

# Main libraries used.

* Pandas for data manipulation and aggregation.
* Matplotlib and seaborn for visualization and behavior with respect to target variable.
* Numpy for computationally efficient operations.
* Scikit Learn for model training, model optimization and metrics calculation.

# Project Flowchart

* Loading data and Diagnosing the data
* Data Filtering
* EDA of Row data to understand inside correlations
* Feature Engineering
* Feature Selection 
* Model Building
* Model Training and Testing
* Model Evalution & Hyper Perameter tuning

## Explaination
I did a lot of work on this project, let me summarise it.
* Data loading:- Mounted drive to load the CSV file and read it through pd.read_csv.
* Data cleaning:- In this section, I cleaned the data by filling the null values through median and mode. I filled the education and BPMeds column through mode because it is nominal data. I also filled cigsPerDay, totChol, BMI, heartRate, glucose through the median. Because these all are continuous variables and filling it through the mean can affect the model. Because the mean is always affected by outliers.
* EDA :- Performed it to get some useful insights.
* Feature engineering:- Made a new column pulse pressure from sysBP and diaBP by doing subtraction within them. Then I did categorical encoding on the sex column. Handled the imbalance dataset to get an unbiased model and at last, I scaled the feature.

# Model Implemented

* Logistic Regression
* Random Forest Classifier
* XGB Classifier
* K Nearest Neighbor
* Support Vector Classifier

# Conclusion


My selected ML model is Random Forest Classifier. The reason behind it is that it was performing very well with hyperparameter tuning as compared to all other models. I tuned it via grid search cv with recall scoring because grid search is very good when it comes to doing cross-validation on smaller datasets. I chose recall as scoring because it is health care data where we can't bear more false negative numbers.

The final results of the model are almost close to the base model and we have achieved almost 90% test accuracy and test precision, and test roc_auc score where as we have achieved almost 88% test recall.

At the end of the project I did a model explanation in which I got the feature importance according to SHAP. As per SHAP I got the sex, age, education, pulse pressure, and cigarettes per day were four main influencers.

Other methods or models could be used to further improve the model. With the help of a medical expert, we could engineer more features which would in turn help improve the model further.
