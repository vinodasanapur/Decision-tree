# Decision Tree Classification on Play Tennis Dataset

## Overview
This repository contains a Jupyter Notebook that implements a binary classification workflow using a **Decision Tree Classifier** to predict whether tennis will be played based on weather conditions.

---

## Dataset Information
The dataset used in the notebook is `tennis_anyone_1000.xlsx`, which consists of 1,000 records[cite: 1].

### Features
* **Day ID**: Unique identifier for each observation (dropped during preprocessing)[cite: 1].
* **Outlook**: Weather condition (Overcast, Rain, Sunny)[cite: 1].
* **Temperature**: Temperature level (Cool, Mild, Hot)[cite: 1].
* **Humidity**: Humidity level (Normal, High)[cite: 1].
* **Wind**: Wind strength (Weak, Strong)[cite: 1].
* **PlayTennis** *(Target Variable)*: Indicates whether tennis was played (`Yes` or `No`)[cite: 1].

---

## Workflow Summary
1. **Data Loading & Exploration**:
   * Loaded `tennis_anyone_1000.xlsx` using Pandas[cite: 1].
   * Inspected dataset structure (`head()`, `shape`, `nunique()`)[cite: 1].
   * Evaluated target variable class distribution (`651` positive vs `349` negative samples)[cite: 1].

2. **Data Preprocessing & Feature Engineering**:
   * Converted categorical attributes into numerical values using `LabelEncoder` from `scikit-learn`[cite: 1].
   * Removed non-predictive metadata (`Day ID`)[cite: 1].
   * Renamed column `Play Tennis` to `PlayTennis` for consistency[cite: 1].

3. **Data Splitting**:
   * Separated feature variables (`X`) and target variable (`Y`)[cite: 1].
   * Performed an 80/20 train-test split (`test_size=0.2`, `random_state=1`)[cite: 1].

4. **Model Training**:
   * Initialized `DecisionTreeClassifier` from `sklearn.tree`[cite: 1].

---

## Prerequisites & Installation

### Dependencies
Ensure Python 3.x is installed along with the required libraries:
```bash
pip install pandas numpy scikit-learn openpyxl notebook
