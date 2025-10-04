# Fault Diagnosis of IC Engine Gearbox using Voting Classifiers

This project was done as a part of the MHA 3010 (Machine Learning For Automation) course at Vellore Institute of Technology, Chennai.

This project investigates the application of machine learning classifiers and ensemble voting methods for diagnosing faults in an IC engine gearbox using vibration-based analysis.

* [Abstract](#Abstract)
* [Objective](#Objective)
* [Methodology](#Methodology)
* [Results](#Results)
* [Credits](#Credits)

## Abstract:

A gearbox is a critical component of an Internal Combustion (IC) engine, and faults in its operation can lead to severe performance and safety issues. This study explores and compares various classifiers and machine learning models for gearbox fault diagnosis using vibration-based diagnostic techniques.

Vibration signals were measured using a tri-axial accelerometer, with data collected for 1 healthy condition and 4 defect conditions:

- 25% defect
- 50% defect
- 75% defect
- 100% defect

Each condition was tested under three load conditions:

- No load
- 9.6 Nm
- 13.3 Nm

## Objective:

- Extract features from gearbox vibration data using statistical, histogram, and ARMA methods.
- Apply feature selection with J48 decision tree to retain significant features.
- Compare 8 machine learning classifiers and evaluate their fault diagnosis accuracy.
- Apply ensemble voting classifiers to improve performance, especially where statistical features lagged.

## Methodology:

1. Signal Acquisition → Vibration data collected under 3 load conditions using tri-axial accelerometer and eddy current dynamometer.
2. Feature Extraction →
   - Statistical features
   - Histogram features
   - ARMA (Auto Regressive Moving Average) features
3. Feature Selection → J48 decision tree pruning to keep only the most relevant features.
4. Classification → 8 ML classifiers applied on selected features.
   - Support Vector Machine (SVM)
   - Multi-layer Perceptron (MLP)
   - Logistics (LO)
   - Random Forest (RF)
   - J48
   - Logistic Model Tree (LMT)
   - Naive Bayes (NB)
   - k - Nearest neighbor (k-NN)
6. Ensemble Learning → Voting classifier applied for statistical features to improve accuracy.
7. Performance Evaluation → Accuracy compared across individual and ensemble classifiers.

<img width="690" height="1108" alt="image" src="https://github.com/user-attachments/assets/db19a5a5-a23d-40a1-bdf5-a83dbda5d445" />

## Results:

- Histogram and ARMA features achieved 100% accuracy across most load conditions.
- Voting classifiers improved accuracy for statistical features by 3.33% under Load 2 (13.3 Nm).
- For Load 2, ensemble models with 2, 3, 4, and 5-class combinations achieved 100% accuracy.
- 2-class ensemble was chosen as the best trade-off between accuracy and computational efficiency.

To Know more about the project, read the Research Article named ``` GearBox Fault Diagnosis.pdf ``` in this repo

## Credits:

Dataset: Provided by Prof. V. Sugumaran (School of Mechanical and Building Sciences, VIT University).

⚠️ Note: Dataset is not included in this repository. All vibration signal data was collected in Prof. V. Sugumaran’s lab and cannot be redistributed.
