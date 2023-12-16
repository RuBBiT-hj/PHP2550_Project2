# PHP2550_Project2

## Title

Tracheostomy/Death Prediction Model in Neonates with Severe Bronchopulmonary Dysplasia at 36-week and 44-week Gestational Age

## Description

### Background

Bronchopulmonary dysplasia (BPD) is a chronic lung condition affecting 10,000 to 15,000 premature infants annually in the United States. Despite advances in neonatal care, the number of severe BPD cases remain steady, particularly among extremely low birth weight (ELBW) infants (Kalikkot Thekkeveedu et al. 2017). 

### Methods

This study addresses the critical need for effective prediction models for composite BPD outcomes - the potential need for tracheostomy and death as well as timing. Based on the records of infants with severe BPD across the US and Sweden from BPD Collaborative Registry (n = 985 and n = 615 at 36 weeks and 44 weeks, respectively), we developed three predictor models at each timing, lasso regression with and without center and multilevel lasso regression with center as a random effect. Multiple imputation was performed to address missing data.

### Results

The fitted models are evaluated on the validation set split from the original data, and the multilevel lasso model has the best performance overall(AUC = 0.810 and 0.855). Considering measurements at 44-week improved the performance of all three models. Our findings reveal significant variability in outcomes across different centers, underscoring the importance of considering clinical setting heterogeneity and timing. Meanwhile, the estimates agree that ventilation support, inspired oxygen, prenatal corticosteriod, and hospital discharge gestational age are the most significant predictors, consistent with the existing literature. However, limitations such as potential bias due to variable missing proportions across centers and the challenge of predicting outcomes for centers not represented in the training data were acknowledged. Also, the resulting model need to adjust for calibration.

### Conclusion

In conclusion, this study provides a prediction model for BPD outcomes with easily accessible clinical measurements, and it accommodates the complexity of clinical settings and measurements at different timing. These results potentially lead to individualized care for premature infants with severe BPD at early stages.

## Main Results

Model performance on the evaluation data set at 36 weeks. The values are obtained at the optimal threshold of each model determined by Youden’s J statistics.

<table>
<thead>
  <tr>
    <th></th>
    <th>Lasso (with center)</th>
    <th>Lasso (without center)</th>
    <th>Multilevel lasso</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Threshold </td>
    <td>0.104</td>
    <td>0.138</td>
    <td>0.135</td>
  </tr>
  <tr>
    <td>Sensitivity</td>
    <td>0.769</td>
    <td>0.742</td>
    <td>0.780</td>
  </tr>
  <tr>
    <td>Specificity</td>
    <td>0.772</td>
    <td>0.773</td>
    <td>0.762</td>
  </tr>
  <tr>
    <td>AUC</td>
    <td>0.793</td>
    <td>0.781</td>
    <td>0.810</td>
  </tr>
  <tr>
    <td>F-score</td>
    <td>0.551</td>
    <td>0.537</td>
    <td>0.548</td>
  </tr>
</tbody>
</table>

Model performance on the evaluation data set at 44 weeks. The values are obtained at the optimal threshold of each model determined by Youden’s J statistics.

<table>
<thead>
  <tr>
    <th></th>
    <th>Lasso (with center)</th>
    <th>Lasso (without center)</th>
    <th>Multilevel lasso</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Threshold </td>
    <td>0.191</td>
    <td>0.211</td>
    <td>0.212</td>
  </tr>
  <tr>
    <td>Sensitivity</td>
    <td>0.813</td>
    <td>0.806</td>
    <td>0.819</td>
  </tr>
  <tr>
    <td>Specificity</td>
    <td>0.809</td>
    <td>0.770</td>
    <td>0.771</td>
  </tr>
  <tr>
    <td>AUC</td>
    <td>0.858</td>
    <td>0.849</td>
    <td>0.855</td>
  </tr>
  <tr>
    <td>F-score</td>
    <td>0.555</td>
    <td>0.512</td>
    <td>0.519</td>
  </tr>
</tbody>
</table>

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