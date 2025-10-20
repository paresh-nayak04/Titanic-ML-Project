# Titanic Survival Prediction – Machine Learning Project

## Project Overview
The **Titanic Survival Prediction** project aims to predict whether a passenger survived the Titanic disaster using machine learning. The dataset contains passenger information such as age, gender, class, fare, and family relationships. This project demonstrates an end-to-end ML workflow from **data preprocessing** to **model training**, **evaluation**, and **visualization**.

---

## Objective
- Predict passenger survival (0 = Did Not Survive, 1 = Survived).  
- Generate a **submission-ready CSV** suitable for the [Kaggle Titanic competition](https://www.kaggle.com/c/titanic).  
- Learn practical ML concepts including preprocessing, feature engineering, and model evaluation.

---

## Dataset
- **Source:** [Kaggle Titanic dataset](https://www.kaggle.com/c/titanic/data)  
- **Files included:**  
  - `train.csv` – labeled training data  
  - `test.csv` – unlabeled test data for prediction  
  - `gender_submission.csv` – sample submission format  

---

## Features
- **Pclass:** Passenger class (1st, 2nd, 3rd)  
- **Sex:** Male/Female  
- **Age:** Age of passenger  
- **SibSp:** Number of siblings/spouses aboard  
- **Parch:** Number of parents/children aboard  
- **Fare:** Ticket fare  
- **Embarked:** Port of embarkation (C, Q, S)  

**Optional Feature Engineering:**  
- `FamilySize` = `SibSp + Parch + 1`  
- Titles extracted from Name (Mr, Mrs, Miss, etc.)

---

## Workflow

### 1. Data Preprocessing
- Checked for missing values and handled them:  
  - `Age` → median  
  - `Fare` → median  
  - `Embarked` → mode  
- Dropped irrelevant columns (`Cabin`, `Ticket`, `Name`)  
- Encoded categorical variables (`Sex`, `Embarked`)  

### 2. Exploratory Data Analysis (EDA)
- **Visualizations:**  
  - Survival count  
  - Survival by gender and passenger class  
  - Age distribution vs survival  
  - Fare vs survival  
  - Family size vs survival  
  - Correlation heatmap  

### 3. Model Training
- **Models used:**  
  - Random Forest Classifier (primary)  
  - Logistic Regression (baseline)  
  - Optional: XGBoost  
- **Evaluation:**  
  - Accuracy score  
  - Confusion matrix  
  - Classification report  

### 4. Prediction & Submission
- Applied trained model on `test.csv`  
- Generated `titanic_submission.csv` for Kaggle submission  

---

## Tools & Libraries
- **Python**  
- **Pandas** & **NumPy** – data manipulation  
- **Seaborn** & **Matplotlib** – visualization  
- **Scikit-learn** – model training and evaluation  
- Optional: **XGBoost**  

---

## Usage
1. Open notebook in [Google Colab](https://colab.research.google.com/)  
2. Run all cells to:  
   - Load and preprocess data  
   - Generate visualizations  
   - Train and evaluate model  
   - Predict survival and create submission file  
3. Upload `titanic_submission.csv` to Kaggle for scoring  

---

## Key Learnings
- Data preprocessing and handling missing values  
- Encoding categorical variables for ML models  
- Feature engineering for better accuracy  
- Training, evaluating, and selecting ML models  
- Visualizing trends to understand data  
- End-to-end ML workflow and Kaggle submission process  
