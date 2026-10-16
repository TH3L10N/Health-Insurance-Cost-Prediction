# Health Insurance Cost Prediction

## 💡 Project Overview

This project uses machine learning regression models to predict yearly medical insurance charges based on customer attributes such as age, BMI, smoking status, and other demographic information.

The goal is to compare different regression models and identify the model that achieves the best predictive performance. The project also explores deploying the best-performing model through an interactive Gradio web application.

## 🎯 Objectives

- Analyze and preprocess the insurance dataset.
- Explore relationships between customer attributes and medical charges.
- Train and evaluate four regression models.
- Compare model performance using standard regression metrics.
- Identify the best-performing model based on test-set results.

## 📊 Dataset

**Source:** [Medical Cost Personal Dataset — Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)

**File:** `insurance.csv`

The dataset contains 1,338 rows and 7 columns.

| Feature | Description |
|---|---|
| `age` | Customer age |
| `sex` | Customer sex |
| `bmi` | Body mass index |
| `children` | Number of dependents |
| `smoker` | Smoking status |
| `region` | Residential region |
| `charges` | Yearly medical insurance charges in USD (target) |

## 🛠️ Tools and Libraries

- **Python** — Main programming language.
- **Pandas and NumPy** — Data manipulation and numerical computations.
- **Matplotlib and Seaborn** — Data visualization and exploratory data analysis.
- **Scikit-learn** — Regression models, preprocessing pipelines, data splitting, and evaluation.
- **Gradio** — Interactive web application interface.

## ⚙️ Methodology

1. **Data Loading and Inspection:** Loaded the dataset, inspected its dimensions, checked for missing values, and removed duplicate records.
2. **Data Preprocessing:** Encoded categorical features into numerical representations.
3. **Exploratory Data Analysis (EDA):** Examined feature relationships using correlation analysis and visualizations.
4. **Data Splitting:** Split the data into training (80%) and testing (20%) sets using `random_state=42`.
5. **Model Training:** Trained four regression models.
6. **Model Evaluation:** Compared model predictions using MAE, MSE, RMSE, and R².
7. **Deployment:** Prepared a Gradio interface for interactive predictions using the selected model.

## 🤖 Models

The following regression models were evaluated:

- **Simple Linear Regression:** Predicts charges using a single feature.
- **Multiple Linear Regression:** Uses multiple features to predict charges.
- **Polynomial Regression:** Uses degree-2 polynomial features to model nonlinear relationships.
- **K-Nearest Neighbors (KNN) Regression:** Uses a distance-based approach with feature scaling.

## 📈 Model Comparison

The following results are recorded for the test set:

| Model | MAE | MSE | RMSE | R² Score |
|---|---:|---:|---:|---:|
| Simple Linear Regression | 5830.64 | 60,039,298.53 | 7748.50 | 0.6733 |
| Multiple Linear Regression | 4173.29 | 35,404,505.77 | 5950.17 | 0.8073 |
| **Polynomial Regression** | **2802.94** | **20,912,088.19** | **4572.97** | **0.8862** |
| KNN Regression | 3042.13 | 24,548,981.82 | 4954.69 | 0.8664 |

### Evaluation Metrics

- **MAE (Mean Absolute Error):** Average absolute difference between actual and predicted values.
- **MSE (Mean Squared Error):** Average squared prediction error.
- **RMSE (Root Mean Squared Error):** Square root of MSE, expressed in the target variable's units.
- **R² Score:** Measures how well the model explains variation in the target variable.

## 🏆 Conclusion

Based on the recorded test-set results, **Polynomial Regression** performed best among the four evaluated models.

It achieved an R² score of **0.8862** and an RMSE of **4572.97 USD**, along with the lowest MAE and MSE.

These results suggest that polynomial features helped capture nonlinear patterns in the dataset. However, performance may vary on new data.

## 🌐 Web Application

The project describes a Gradio interface that allows users to enter customer attributes and obtain predicted yearly medical insurance charges.

The interface inputs include:

- Age
- Sex
- BMI
- Number of children
- Smoking status
- Region

**Note:** Add the application launch instructions or a public demo link here once they are available.

## 📂 Project Structure

```text
Health-Insurance-Cost-Prediction/
├── data/
│   └── insurance.csv
├── notebook/
│   └── Task1_Insurance_Regression_STUDENT.ipynb
├── .gitignore
└── README.md
```

*Update this structure if your actual repository uses different file locations.*

## 🚀 Installation and Usage

### 1. Clone the Repository

```bash
git clone https://github.com/TH3L10N/Health-Insurance-Cost-Prediction.git
cd Health-Insurance-Cost-Prediction
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available yet, install the main libraries with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn gradio jupyter
```

### 3. Run the Notebook

Open the notebook using Jupyter Notebook or VS Code and execute the cells in order.

Make sure the dataset path in the notebook matches the actual location of `insurance.csv`.

## 👤 Author

**TH3L10N**

GitHub: [@TH3L10N](https://github.com/TH3L10N)

## 📚 References

- [Medical Cost Personal Dataset — Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Gradio Documentation](https://www.gradio.app/docs)
