# Assignment 5 – Adversarial Attack Audit of COMPAS Models
Name: Rafay Raza 
GWID: G40856805

## Purpose of the Analysis
The purpose of this analysis is to evaluate the security and vulnerability of machine learning models trained on the COMPAS two-year recidivism dataset under adversarial conditions. The audit focuses on three attack classes: evasion, data poisoning, and membership inference.

A projected gradient descent (PGD) evasion attack is implemented to test how small input perturbations affect model predictions and fairness outcomes across racial groups. A label-flip poisoning attack is simulated to examine how training data manipulation can degrade fairness while remaining undetected by standard performance metrics. Membership inference is evaluated using a shadow-model approach to assess potential privacy leakage from the trained models.

The analysis compares logistic regression and gradient-boosted tree models to determine their relative vulnerability to these attacks and to assess how adversarial behavior impacts both performance and fairness metrics such as false positive rates and Adverse Impact Ratio (AIR).

## Python Libraries Used
The following Python libraries were used in this assignment:
* pandas
* numpy
* matplotlib
* scikit-learn
* scipy

## Instructions for Reproducing the Results
To reproduce the results:
1. Install the required Python libraries:
2. pip install pandas numpy matplotlib scikit-learn scipy
3. Open the Jupyter Notebook file: `Individual_Assignment_5_Rafay_Raza_G40856805.ipynb`
4. Run all cells in the notebook from top to bottom. The notebook will:
   * Load and preprocess the COMPAS dataset
   * Train logistic regression and gradient-boosted models
   * Establish a clean-model fairness baseline (FPR and AIR by race)
   * Implement a PGD evasion attack and evaluate its impact across different epsilon values
   * Simulate a label-flip poisoning attack and track AUC and AIR degradation
   * Identify stealth attack regions where fairness degrades without performance loss
   * Run a membership inference attack using a shadow-model pipeline
   * Evaluate privacy risk using ROC curves and confidence gap analysis
   * Summarize findings across all attack types and discuss mitigation strategies

The dataset is loaded directly from the ProPublica COMPAS dataset repository:
https://raw.githubusercontent.com/propublica/compas-analysis/master/compas-scores-two-years.csv

## AI Acknowledgment
AI tools were used for general programming guidance, debugging, and assistance with Markdown formatting and grammar.
