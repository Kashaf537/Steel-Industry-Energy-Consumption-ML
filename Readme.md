# ⚡ Steel Industry Energy Consumption Analysis & Baseline Regression Modeling

## 📖 Project Overview

This project was completed as part of the **ITSimplera AI/ML Internship**. The objective was to analyze an industrial energy consumption dataset, engineer meaningful features, and build baseline machine learning regression models to predict electricity usage (`Usage_kWh`).

The project is divided into two main parts:

- **Part 1:** Deep Exploratory Data Analysis (EDA) & Feature Engineering
- **Part 2:** Baseline Regression Modeling

The final engineered dataset is used to train and evaluate multiple regression models for predicting energy consumption.

---

# 📂 Repository Structure

```
├── data/
│   ├── Steel Industry Energy.csv
│   └── engineered_energy_dataset.csv
│
├── week2_eda.ipynb
│── week2_baseline_models.ipynb
│   
│
├── images/
│   ├── dataset_overview.png
│   ├── correlation_heatmap.png
│   ├── boxplot.png
│   ├── rmse_comparison.png
│   └── predicted_vs_actual.png 
│   └── evaluation_metric_models.png
│
├── requirements.txt
├── README.md
```

---

# 📊 Dataset Information

**Dataset:** Steel Industry Energy Consumption

The dataset contains electricity consumption records collected from an industrial manufacturing process.

### Original Features

- date
- Usage_kWh *(Target Variable)*
- Lagging_Current_Reactive.Power_kVarh
- Leading_Current_Reactive_Power_kVarh
- CO2(tCO2)
- Lagging_Current_Power_Factor
- Leading_Current_Power_Factor
- NSM
- WeekStatus
- Day_of_week
- Load_Type

---

# 📥 Dataset Download

The dataset is available through the following Google Drive link:

**Google Drive:**  
*https://docs.google.com/spreadsheets/d/1NyC750ZBipJyxifVBqoJJso8MJFEWf0X/edit?usp=drive_link&ouid=101548115907938380372&rtpof=true&sd=true*

After downloading:

1. Create a folder named **data** inside the project directory.
2. Place the downloaded dataset inside the **data/** folder.
3. Run the notebooks.

---

# ⚙️ Environment Setup

## Clone the repository

```bash
git clone https://github.com/Kashaf537/Steel-Industry-Energy-Consumption.git
```

## Navigate into the project

```bash
cd Steel-Industry-Energy-Consumption
```

## Install dependencies

```bash
pip install -r requirements.txt
```

## Launch Jupyter Notebook

```bash
jupyter notebook
```

---

# 🛠️ Feature Engineering

The following features were engineered from the original dataset:

- Hour (Extracted from Date)
- Month
- Day_of_Week
- Week_Status
- PowerFactorRatio
- HighLoad (Binary feature based on the 75th percentile of Usage_kWh)

The original **date** column and target leakage features were removed before model training.

---

# 📈 Exploratory Data Analysis (EDA)

The following analyses were performed:

- Dataset overview
- Missing value analysis
- Duplicate record detection
- Summary statistics
- Correlation analysis
- Feature correlation with Usage_kWh
- Monthly energy consumption trend
- Outlier detection using box plots
- Data quality assessment

### Key Findings

- No missing values were found.
- No duplicate records were present.
- Several high-value outliers were detected in energy consumption.
- CO2 emissions showed an extremely strong positive correlation with energy usage.
- Reactive power also exhibited a strong relationship with electricity consumption.

---

# 🤖 Baseline Regression Modeling

Four regression models were trained:

- Linear Regression
- Ridge Regression
- Decision Tree Regressor
- Random Forest Regressor

### Data Preprocessing

- Removed target leakage features.
- Applied One-Hot Encoding to categorical variables.
- Performed an 80/20 Train-Test Split.
- Used `random_state=42` for reproducibility.

---

# 📏 Evaluation Metrics

Each model was evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

Additionally,

- 5-Fold Cross Validation
- Mean Cross Validation RMSE

were performed to assess model generalization.

---

# 📊 Results

The notebook includes:

- RMSE comparison bar chart
- Predicted vs Actual scatter plot
- Cross-validation results
- Model comparison

The best-performing model was selected based on the lowest RMSE and highest R² score.

---

# 📷 Screenshots

Add screenshots of important outputs here.

Suggested screenshots:

- Dataset Overview
screenshots\DatasetOverview.png
- Correlation Heatmap
screenshots\corr.png
- Box Plot
screenshots\BoxPlot.png
- RMSE Comparison
screenshots\Test RMSE.png
- Predicted vs Actual Plot
screenshots\predicted_vs_actual.png
Cross Validation results
screenshots\crossval_results.png
Average Energy Usage
screenshots\Avg_energy_usage.png
Evaluation Metrics for all models
screenshots\evaluation_metric.png
```

---

# 📌 Conclusions

This project demonstrates the complete workflow of a machine learning regression problem, including:

- Data understanding
- Data preprocessing
- Feature engineering
- Exploratory data analysis
- Baseline regression modeling
- Model evaluation
- Model selection

The project establishes a strong baseline for future work involving hyperparameter tuning, feature selection, and advanced machine learning techniques.

---

# 🧰 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📄 Requirements

Install all required packages using:

```bash
pip install -r requirements.txt
```

---

# 👨‍💻 Author

**Kashaf Fayyaz**

BS Artificial Intelligence  
COMSATS University Islamabad

GitHub: https://github.com/Kashaf537


---

# ⭐ Acknowledgement

This project was completed as part of the **ITSimplera AI/ML Internship**, focusing on practical applications of Exploratory Data Analysis, Feature Engineering, and Machine Learning Regression.