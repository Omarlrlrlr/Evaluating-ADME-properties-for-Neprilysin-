# Evaluating-ADME-properties-for-Neprilysin-

In this code we built a machine learning model to predict the potency of de novo chemical coumpounds based on (pIC50) index against Neprilysin. The inhibition of Neprilysin topically is very important in anti-aging process, because it degrades various bioactive peptides, involved in inflammation and collagen degradation.

## 1- Data extraction
We used he ChemBL database to extract Neprilysin compounds, and retrieving bioactivity data.

## 2- Data pre-processing
Bsed on the feature (standard_value) we sorted our compounds into active and inactive ones, with the elimination of the intermediate ones, we fixed a threshold to differentiate between them, where compounds reprensenting a value bigger than 10000nM are considered as inactive, and those lower than 1000nM as active. Than we calculated the Lepinski Descriptors and the Molecular fingerprints. And converting the IC50 values to pIC50 the nagative logarithm to normalize the values distribution.

## 3- Building the model
The variable to predict is the pIC50 one, it will help us to categorize other compounds a biologicaly active or inactive, and the x variables where the pubchem molecular descriptors, that we calculated using PaDel descriptors. We used in this project a Random forest regressor

## 4- Evaluation 
Many metrics were used to evaluate the model as R squared, MSE.
