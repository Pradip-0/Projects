This project was a hackathon project conducted by PharmaQuant. Here, the data consists of information from all diabetic hospitals in the US. Our goal is to analyse the data
and make some insights to reduce the readmission rate.
Here, the KNN regression imputation technique is used to impute the missing values, and then exploratory data analysis is performed. 
Key insights from EDA:
- Females have a slightly higher readmission count. i.e., females are slightly more likely to be readmitted.
- Caucasians have the highest readmission count.
- Patients who are discharged home are more likely to be readmitted.
- There is no pattern between time spent in hospital and readmission, i.e., period in hospital has nothing to do with the readmission.
- The box plots show that those patients on whom most lab procedures are performed are more likely to be readmitted.
- The age group 70-80 has the highest readmission rate.

  After the EDA part, some models are fitted to the data, like decision tree, logistic regression, xgboost, and random forest. But all these models
have similar accuracy. So, the logistic regression model and the XGBoost model are selected for further analysis.

 As the XGBoost model has slightly greater accuracy so our results are obtained considering this model. The top 10 features which are important for predicting readmission
 are:
                                            Feature  Importance
9                             num__number_inpatient    0.100820
1                     num__discharge_disposition_id    0.040074
2                          num__admission_source_id    0.022201
113                             cat__diabetesMed_No    0.021639
10                            num__number_diagnoses    0.019369
8                             num__number_emergency    0.018461
7                            num__number_outpatient    0.018268
56   cat__medical_specialty_ObstetricsandGynecology    0.017178
105                      cat__max_glu_serum_Missing    0.016307
39          cat__medical_specialty_Emergency/Trauma    0.015988

  In conclusion, the hospitals should work on these areas to reduce their readmission rate.
