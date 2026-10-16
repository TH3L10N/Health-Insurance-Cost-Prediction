# Health Insurance Cost Prediction

## 💡 Project Overview
This project aims to build and evaluate several machine learning regression models to predict yearly medical charges (`charges`) for insurance customers based on demographic and health attributes (such as age, BMI, smoking status, etc.). Accurate predictions enable the insurance company to determine appropriate and fair policy pricing. Additionally, an interactive web application is deployed using Gradio for real-time predictions.

## Business Brief
An insurance company wants to predict the yearly medical charges of each customer, so it can price its policies correctly.

## Objective
Build four regression models, compare them, and choose the one that predicts `charges` most accurately.

## Dataset
- **Source:** [Kaggle - Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance) (File: `insurance.csv`)
- **Features & Target:**
  - `age`: Customer age
  - `sex`: male / female (mapped to 0/1)
  - `bmi`: Body mass index
  - `children`: Number of dependents
  - `smoker`: yes / no (mapped to 0/1)
  - `region`: Residential region (mapped numerically)
  - `charges`: Yearly medical charges in USD (**Target**)

---

## Methodology & Steps
1. **Data Loading & Inspection:** Loaded the dataset, checked dimensions (1338 rows, 7 columns), handled missing values, and dropped duplicates.
2. **Data Preprocessing:** Encoded categorical features (`sex`, `smoker`, `region`) into numerical values.
3. **Exploratory Data Analysis (EDA):** Calculated correlation matrices and plotted feature relationships (notably `age` vs `charges` colored by `smoker`).
4. **Data Splitting:** Defined `X` and `y`, splitting the dataset into 80% training and 20% testing sets (`random_state=42`).
5. **Model Training:** Built and trained four distinct regression models:
   - Simple Linear Regression
   - Multiple Linear Regression
   - Polynomial Regression (Degree 2 Pipeline)
   - KNN Regression (Pipeline with StandardScaler)
6. **Evaluation & Comparison:** Evaluated all models on the test set using MAE, MSE, RMSE, and $R^2$ score.
7. **Deployment:** Deployed the best performing model as an interactive web application using **Gradio**.

---

## Model Comparison Results

| Model | MAE | MSE | RMSE | R² Score |
| :--- | :---: | :---: | :---: | :---: |
| **Simple Linear Regression** | 5830.64 | 60,039,298.53 | 7748.50 | 0.6733 |
| **Multiple Linear Regression** | 4173.29 | 35,404,505.77 | 5950.17 | 0.8073 |
| **Polynomial Regression** | **2802.94** | **20,912,088.19** | **4572.97** | **0.8862** |
| **KNN Regression** | 3042.13 | 24,548,981.82 | 4954.69 | 0.8664 |

---

## Conclusion
*Polynomial Regression* is the best model among the four tested regression models. It achieved the highest R² score of **0.8862** and the lowest RMSE of **4572.97** on the test set. It outperforms the other models because polynomial features effectively capture the non-linear relationships and interaction effects between variables such as smoking, BMI, and age.

---

## Web App Deployment (Gradio)
The best model (Polynomial Regression) has been integrated into a Gradio interface allowing users to input customer parameters (Age, Sex, BMI, Children, Smoker, Region) and instantly receive the predicted yearly medical charges.# Health-Insurance-Cost-Prediction
---
## 🛠️ Tools & Libraries Used
The project is implemented in **Python** using industry-standard data science and machine learning libraries:
- **Pandas & NumPy**: For data manipulation, cleaning, and numerical computations.
- **Scikit-Learn**: For building regression models, pipelines, data splitting, and performance evaluation.
- **Matplotlib & Seaborn**: For exploratory data analysis (EDA) and data visualization.
- **Gradio**: For deploying the best model as an interactive web app.
---
# Health-Insurance-Cost-Prediction
## 📂 Project Structure
Health-Insurance-Cost-Prediction/
│
├── data/
│   └── insurance.csv         # Original dataset
│
├── notebook/
│   └── Task1_Insurance_Regression_STUDENT.ipynb  # Jupyter Notebook containing code, analysis, and outputs
│
├── .gitignore                # Files and directories to ignore by Git
└── README.md                 # Project documentation
