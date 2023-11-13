# PHP2550_Project2

## Title

Tracheostomy/Death Prediction Model in Neonates with Severe Bronchopulmonary Dysplasia at 36-week Gestational Age

## Description

### Background

Bronchopulmonary dysplasia (BPD) is a chronic lung condition affecting 10,000 to 15,000 premature infants annually in the United States. Despite advances in neonatal care, the number of severe BPD cases remain steady, particularly among extremely low birth weight (ELBW) infants.

### Methods

This study addresses the critical need for effective prediction models for composite BPD outcomes - the potential need for tracheostomy and death. Based on the records of infants with severe BPD across the US and Sweden from BPD Collaborative Registry (n = 985), we developed three predictor models: Lasso regression with and without center and multilevel lasso regression with center as a random effect. Multiple imputation was performed to address missing data, and 5-fold cross-validation was performed to optimize the hyperparameter.

### Results

The fitted models are evaluated on the validation set split from the original data, and the mul- tilevel lasso model has the best performance (AUC = 0.910). Our findings reveal significant variability in outcomes across different centers, underscoring the importance of considering clinical setting heterogeneity. Meanwhile, the estimates agree that ventilation support, inspired oxygen, prenatal corticosteriod, and hos- pital discharge gestational age are the most significant predictors, consistent with the existing literature. However, limitations such as potential bias due to variable missing proportions across centers and the chal- lenge of predicting outcomes for centers not represented in the training data were acknowledged. Also, one of the predictors hospital discharge gestational age may need an additional model to simulate.

### Conclusion

This study provides a prediction model for BPD outcomes with easily accessible clinical measurements, and it accommodates the complexity of clinical settings. These results potentially lead to individualized care for premature infants with severe BPD at early stages.

## Code Availability

The code used for processing, EDA, and modeling are attached after the main text.

### Package

R version 4.3.0

* boot (1.3-28.1)
* glmmLasso (1.6.3)
* gtsummary (1.7.2)
* kableExtra (1.3.4)
* mice (3.16.0)
* pROC (1.18.2)
* tidyverse (2.0.0)

## Acknowledgement

This project is a collaboration with Dr. Chris Schmid in the Biostatistics Department (Christopher_Schmid@brown.edu). This project is advised by Dr. Alice Paul (alice_paul@brown.edu)