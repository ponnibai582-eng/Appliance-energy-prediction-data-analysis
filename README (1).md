# ⚡ Energy Data Analysis & Appliance Energy Prediction

## 📌 Project Overview

This project focuses on **Energy Data Analysis and Machine Learning-based Regression** to predict **Appliance Energy Consumption**.

The project follows a complete Data Science workflow, starting from data collection and preprocessing to exploratory data analysis, feature selection, regression modelling, and model evaluation.

The main objective is to understand the factors affecting energy consumption and build a machine learning model that can predict appliance energy usage.

---

## 👩‍💻 Project Details

- **Project Name:** Energy Data Analysis & Appliance Energy Prediction
- **Author:** Ponnibai G
- **Machine Learning Type:** Supervised Learning – Regression
- **Target Variable:** ApplianceEnergy
- **Dataset:** Energydata.csv
- **Dataset Source:** UCI Machine Learning Repository

---

## 🎯 Objectives

- Understand and analyze the energy consumption dataset.
- Clean and preprocess the dataset.
- Handle missing values and duplicate records.
- Perform Exploratory Data Analysis (EDA).
- Analyze correlations between features.
- Identify important features for prediction.
- Apply different regression algorithms.
- Evaluate and compare model performance.
- Select the best-performing regression model.

---

## 📊 Dataset Description

The dataset contains **19,735 records and 29 original columns**.

The data contains information related to:

- Appliance energy consumption
- Lighting energy
- Indoor temperature
- Indoor humidity
- Outdoor temperature
- Outdoor humidity
- Atmospheric pressure
- Wind speed
- Visibility
- Dew point
- Date and time information

The original date information was transformed into useful time-based features such as:

- Year
- Month
- Hour
- Day of Week

The target variable used for prediction is **ApplianceEnergy**.

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Loading
     ↓
Data Cleaning
     ↓
Missing Value & Duplicate Check
     ↓
Date Conversion
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
Correlation Analysis
     ↓
Feature Selection
     ↓
Train-Test Split
     ↓
Feature Scaling
     ↓
Regression Models
     ↓
Model Evaluation
     ↓
Model Comparison
     ↓
Best Model Selection
     ↓
Energy Prediction
```

---

## 🧹 Data Preprocessing

### 1. Load Dataset
The `Energydata.csv` dataset was loaded using Pandas.

### 2. Missing Value Check
Missing values were checked across all columns. The original dataset contained **no missing values**.

### 3. Duplicate Check
Duplicate records were checked.

```text
Duplicate Rows = 0
```

### 4. Date Conversion
The date column was converted into datetime format.

### 5. Feature Engineering
Date information was converted into:

- Year
- Month
- Hour
- Day of Week

### 6. Feature and Target Separation

```text
X → Predictor Features
y → ApplianceEnergy
```

---

## 📈 Exploratory Data Analysis (EDA)

The following EDA techniques were performed:

- Descriptive Statistics
- Correlation Matrix
- Heatmap
- Boxplot Analysis
- Skewness Analysis
- Outlier Analysis

Descriptive statistics included mean, standard deviation, minimum, maximum and quartiles.

---

## 🔍 Feature Selection

Correlation-based feature selection was performed.

Features having an absolute correlation greater than **0.05** were selected in the notebook.

Some important relationships included:

| Feature | Approx. Correlation |
|---|---:|
| Hour | 0.217 |
| Lights | 0.197 |
| Outdoor Humidity | 0.152 |
| Temp2 | 0.120 |
| Outdoor Temperature | 0.099 |
| Wind Speed | 0.087 |

> **Note:** Correlation indicates association between variables; it does not prove causation.

---

## 🚨 Outlier Analysis

The **IQR (Interquartile Range)** method was explored for detecting and treating outliers.

```text
Q1 = 25th Percentile
Q3 = 75th Percentile

IQR = Q3 - Q1

Lower Limit = Q1 - 1.5 × IQR
Upper Limit = Q3 + 1.5 × IQR
```

Extreme values were clipped within the calculated limits.

---

## ✂️ Train-Test Split

The dataset was divided into:

```text
80% → Training Data
20% → Testing Data
```

`random_state = 42` was used to make the split reproducible.

---

## ⚖️ Feature Scaling

`StandardScaler` was prepared for standardizing the features.

Scaling is especially useful for machine learning algorithms that are sensitive to differences in feature magnitude.

---

# 🤖 Machine Learning Algorithms

Four regression algorithms were compared.

### 1. Linear Regression
A basic regression algorithm that models a linear relationship between input features and the target variable.

### 2. Decision Tree Regression
A non-linear model that makes predictions using a series of decision rules.

### 3. Random Forest Regression
An ensemble model that combines multiple decision trees to improve prediction performance.

### 4. Gradient Boosting Regression
An ensemble technique where trees are built sequentially, with each new tree attempting to reduce the errors of the previous models.

---

# 📊 Model Evaluation

The models were evaluated using:

### MAE – Mean Absolute Error
Measures the average absolute difference between actual and predicted values.

**Lower MAE is better.**

### MSE – Mean Squared Error
Measures the average squared prediction error.

**Lower MSE is better.**

### RMSE – Root Mean Squared Error
RMSE is the square root of MSE.

```text
RMSE = √MSE
```

**Lower RMSE is better.**

### R² Score
R² measures how well the model explains the variation in the target variable.

**Higher R² is better.**

---

# 🏆 Model Performance

| Model | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Linear Regression | 0.06 | 0.01 | 0.11 | 0.82 |
| Decision Tree | 0.03 | 0.00 | 0.05 | 0.95 |
| Random Forest | 0.05 | 0.01 | 0.07 | 0.92 |
| **Gradient Boosting** | **0.04** | **0.00** | **0.05** | **0.96** |

---

# 🥇 Best Model

## Gradient Boosting Regression

Among the four tested algorithms, **Gradient Boosting achieved the highest recorded R² score of 0.96**.

Therefore, Gradient Boosting was selected as the preferred model among the tested models.

```text
Best Model: Gradient Boosting
R² Score: 0.96
RMSE: 0.05
```

---

# 🛠️ Technologies Used

### Programming Language
- Python

### Libraries
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Development Environment
- Jupyter Notebook
- Google Colab / VS Code

### Machine Learning
- Linear Regression
- Decision Tree Regression
- Random Forest Regression
- Gradient Boosting Regression

---

# 📁 Project Structure

```text
Energy-Data-Analysis/
│
├── Energydata.csv
├── Energy_Data_Analysis.ipynb
├── README.md
│
└── outputs/
    ├── correlation_heatmap.png
    ├── boxplots.png
    └── model_comparison.png
```

---

# 🚀 How to Run the Project

### Step 1 – Clone the Repository

```bash
git clone https://github.com/your-username/energy-data-analysis.git
```

### Step 2 – Open the Project

```bash
cd energy-data-analysis
```

### Step 3 – Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Step 4 – Open Jupyter Notebook

```bash
jupyter notebook
```

### Step 5 – Run the Notebook

Open the project notebook and run the cells sequentially from data loading to model evaluation.

---

# 📌 Key Findings

- The dataset contains **19,735 records** and **29 original features**.
- No missing values were found in the original dataset.
- No duplicate rows were found.
- Time-based features were created from the date information.
- Correlation and EDA were used to identify useful relationships.
- Four regression algorithms were compared.
- Gradient Boosting achieved the highest recorded **R² score of 0.96**.
- The project demonstrates a complete **Data Analysis + Machine Learning Regression workflow**.

---

# 🔮 Future Improvements

- Hyperparameter tuning
- Cross-validation
- Advanced feature engineering
- Compare additional regression algorithms
- Create an interactive dashboard
- Deploy the model as a web application
- Add real-time energy prediction
- Integrate energy monitoring systems

---

# 🎓 Learning Outcomes

Through this project, the following skills were developed:

- Data Cleaning
- Data Preprocessing
- Exploratory Data Analysis
- Data Visualization
- Feature Engineering
- Feature Selection
- Regression Modelling
- Model Evaluation
- Machine Learning Model Comparison
- Python Data Science Workflow

---

# 📜 Conclusion

This project demonstrates how **Python and Machine Learning** can be used to analyze energy consumption data and build predictive regression models.

After preprocessing the dataset, performing EDA, selecting relevant features, and comparing four regression algorithms, **Gradient Boosting achieved the highest recorded R² score of 0.96**.

The project provides a complete workflow from **raw energy data to machine learning-based appliance energy prediction**.

---

## 👩‍💻 Author

**Ponnibai G**

Data Analysis | Machine Learning | Python

---

⭐ If you find this project useful, consider giving the repository a **star**!
