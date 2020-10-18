# Goal and Overview

The goal of this project was to implement a Linear Regression on a select dataset. I chose to run a multiple logistic regression on the [Heart Failure Prediction](https://www.kaggle.com/andrewmvd/heart-failure-clinical-data) data set with the goal of answering: how strong of a prediction model can be built using these few features, and among this list, which feature is the strongest single predictor of death for patients dealing with a heart condition.

# Motivation

It is natural to want to leverage Machine Learning techniques in the world of health and medicine. In doing so, we can aim to maximize what we can learn from each patient, and better prepare for cases to come. In this particular study, we aim to better understand patients with heart conditions, since it is globally and nationally the leading cause death. 

# Background
This data was provided from [Kaggle](https://www.kaggle.com/andrewmvd/heart-failure-clinical-data), and was based on real patient data gathered in 2015. Using a variety of Machine Learning techniques, they concluded that you could reliably predict survival rates studying serum creatinine and ejection fraction alone.

# Navigation (Need to link notebooks)

[Technical Notebok](https://github.com/miles-frankllin/DATA_602/blob/master/Hw_1/Notebooks/Additional_Notebook.ipynb) -
[Additional NoteBook](https://github.com/miles-frankllin/DATA_602/blob/master/Hw_1/Notebooks/Additional_Notebook.ipynb) -
[Data - Kaggle](https://www.kaggle.com/andrewmvd/heart-failure-clinical-data) - 
[Data - Research Paper](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-1023-5)

# Requirements
<pre>
Languages    : Python 3.8.3
Tools/IDE    : Anaconda
Libraries    : requests, bs4, time, pandas, matplotlib, numpy, scipy, sklearn
</pre>

# Data Sources

### Raw Data
<pre>
File Name      : heart_failure_clinical_records_dataset.csv
URL            : https://www.kaggle.com/andrewmvd/heart-failure-clinical-data
Limitations    : This is not the largest sample size, given the magnitude of the problem it is aiming to solve.
Concerns       : N/A
Dimensions     : 299 rows × 13 columns
Columns        : 
<table class="data last-table">
 <thead class="c-article-table-head">
  <tr>
   <th class="u-text-left">
    Feature
   </th>
   <th class="u-text-left">
    Explanation
   </th>
   <th class="u-text-left">
    Measurement
   </th>
   <th class="u-text-left">
    Range
   </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="u-text-left">
    Age
   </td>
   <td class="u-text-left">
    Age of the patient
   </td>
   <td class="u-text-left">
    Years
   </td>
   <td class="u-text-left">
    [40,..., 95]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Anaemia
   </td>
   <td class="u-text-left">
    Decrease of red blood cells or hemoglobin
   </td>
   <td class="u-text-left">
    Boolean
   </td>
   <td class="u-text-left">
    0, 1
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    High blood pressure
   </td>
   <td class="u-text-left">
    If a patient has hypertension
   </td>
   <td class="u-text-left">
    Boolean
   </td>
   <td class="u-text-left">
    0, 1
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Creatinine phosphokinase
   </td>
   <td class="u-text-left">
    Level of the CPK enzyme in the blood
   </td>
   <td class="u-text-left">
    mcg/L
   </td>
   <td class="u-text-left">
    [23,..., 7861]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    (CPK)
   </td>
   <td class="u-text-left">
   </td>
   <td class="u-text-left">
   </td>
   <td class="u-text-left">
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Diabetes
   </td>
   <td class="u-text-left">
    If the patient has diabetes
   </td>
   <td class="u-text-left">
    Boolean
   </td>
   <td class="u-text-left">
    0, 1
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Ejection fraction
   </td>
   <td class="u-text-left">
    Percentage of blood leaving
   </td>
   <td class="u-text-left">
    Percentage
   </td>
   <td class="u-text-left">
    [14,..., 80]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
   </td>
   <td class="u-text-left">
    the heart at each contraction
   </td>
   <td class="u-text-left">
   </td>
   <td class="u-text-left">
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Sex
   </td>
   <td class="u-text-left">
    Woman or man
   </td>
   <td class="u-text-left">
    Binary
   </td>
   <td class="u-text-left">
    0, 1
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Platelets
   </td>
   <td class="u-text-left">
    Platelets in the blood
   </td>
   <td class="u-text-left">
    kiloplatelets/mL
   </td>
   <td class="u-text-left">
    [25.01,..., 850.00]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Serum creatinine
   </td>
   <td class="u-text-left">
    Level of creatinine in the blood
   </td>
   <td class="u-text-left">
    mg/dL
   </td>
   <td class="u-text-left">
    [0.50,..., 9.40]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Serum sodium
   </td>
   <td class="u-text-left">
    Level of sodium in the blood
   </td>
   <td class="u-text-left">
    mEq/L
   </td>
   <td class="u-text-left">
    [114,..., 148]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Smoking
   </td>
   <td class="u-text-left">
    If the patient smokes
   </td>
   <td class="u-text-left">
    Boolean
   </td>
   <td class="u-text-left">
    0, 1
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    Time
   </td>
   <td class="u-text-left">
    Follow-up period
   </td>
   <td class="u-text-left">
    Days
   </td>
   <td class="u-text-left">
    [4,...,285]
   </td>
  </tr>
  <tr>
   <td class="u-text-left">
    (target) death event
   </td>
   <td class="u-text-left">
    If the patient died during the follow-up period
   </td>
   <td class="u-text-left">
    Boolean
   </td>
   <td class="u-text-left">
    0, 1
   </td>
  </tr>
 </tbody>
</table>
* Table from https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-1023-5/tables/1
</pre>

### Cleaned Data
<pre>
File Name      : heart_failure_clinical_records_dataset-cleaned.csv
URL            : N/A
Limitations    : N/A
Concerns       : N/A
Dimensions     : 279 rows × 13 columns
Columns        : age (int64), anaemia (int64), creatinine_phosphokinase (int64), diabetes (int64),
                 ejection_fraction (int64), high_blood_pressure (int64), platelets (float64), 
                 serum_creatinine (float64), serum_sodium (int64), sex (int64), smoking (int64),
                 time (int64), DEATH_EVENT (int64)
</pre>

# References
<pre>
URL            : https://doi.org/10.1186/s12911-020-1023-5
Author         : Chicco, D., Jurman, G.
Purpose        : The data set found was built on the study in this article.
</pre>
