# Fundamentals of Data Science (FDS) Project

A comprehensive repository for the **Fundamentals of Data Science** laboratory and coursework, covering end-to-end data processing, exploratory data analysis (EDA), probability distributions, statistical hypothesis testing, data visualization, and predictive modeling using Python.

---

## 📌 Project Overview

This repository demonstrates practical data science workflows using an academic dataset of student lifestyle, behavioral, and performance indicators (`dataset.csv`). Each notebook builds sequentially upon fundamental principles of data manipulation, statistical inference, and machine learning.

---

## 📂 Repository Structure

```text
├── dataset.csv        # Student Performance Factors dataset
├── 1.1.ipynb          # Data Ingestion, Inspection & Structural Analysis
├── 1.2.ipynb          # Data Cleaning, Preprocessing & Outlier Treatment
├── 1.3.ipynb          # Descriptive Statistics & Custom Numerical Summaries
├── 1.4.ipynb          # Probability Distributions (PMF, PDF, CDF)
├── 1.5.ipynb          # Hypothesis Testing (Two-Sample t-Test & Chi-Squared Test)
├── 1.6.ipynb          # Simple Linear Regression (From-Scratch Math & Modeling)
├── 1.7.ipynb          # Exploratory Data Visualization & Comparative Plotting
├── requirements.txt   # Environment dependencies
└── README.md          # Project documentation and guide
```

---

## 📊 Dataset Information & Source Attribution

### Source & Licensing
- **Dataset Origin:** [Kaggle - Student Performance Factors Dataset](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors)
- **License / Usage:** Open Database License (ODbL) / Public Domain dedication. Distributed freely for educational, academic, and non-commercial research purposes.
- **Attribution:** The dataset is used here strictly as part of academic coursework for studying statistical techniques and regression analysis. All rights and credit for original collection and curation remain with the dataset creators and contributors.

### Dataset Specifications
- **File Name:** `dataset.csv`
- **Observations:** 317 records × 17 features
- **Domain:** Educational Data Mining / Academic Performance Analytics

### Attributes & Schema

| Feature | Type | Description |
| :--- | :--- | :--- |
| `Hours_Studied` | Numeric | Total study hours invested by the student |
| `Attendance` | Numeric | Class attendance percentage |
| `Parental_Involvement` | Categorical | Level of parental academic involvement (`Low`, `Medium`, `High`) |
| `Access_to_Resources` | Categorical | Availability of study materials/resources (`Low`, `Medium`, `High`) |
| `Extracurricular_Activities` | Categorical | Participation in extracurricular activities (`Yes`, `No`) |
| `Sleep_Hours` | Numeric | Average daily hours of sleep |
| `Previous_Scores` | Numeric | Historical examination score |
| `Motivation_Level` | Categorical | Self-reported student motivation level (`Low`, `Medium`, `High`) |
| `Internet_Access` | Categorical | Access to internet at home (`Yes`, `No`) |
| `Tutoring_Sessions` | Numeric | Count of external tutoring sessions attended per month |
| `School_Type` | Categorical | Type of institution attended (`Public`, `Private`) |
| `Peer_Influence` | Categorical | Influence of peer group (`Positive`, `Neutral`, `Negative`) |
| `Physical_Activity` | Numeric | Weekly physical activity / sports hours |
| `Learning_Disabilities` | Categorical | Indication of learning disabilities (`Yes`, `No`) |
| `Distance_from_Home` | Categorical | Proximity to school (`Near`, `Moderate`, `Far`) |
| `Gender` | Categorical | Student gender (`Male`, `Female`) |
| **`Exam_Score`** | Numeric | **Target Variable:** Final student examination score |

---

## 🔬 Notebook Walkthrough

### `1.1.ipynb` — Data Ingestion & Inspection
- Loading tabular data into pandas DataFrame.
- Dimension inspection (`shape`), column schema, and data types (`dtypes`).
- Positional index head slicing and boundary verification.

### `1.2.ipynb` — Data Preprocessing & Cleaning
- **Missing Value Imputation:** Mode imputation for categorical features (`Distance_from_Home`) and mean imputation for numeric features.
- **Deduplication:** Identification and elimination of duplicate records.
- **Standardization:** Stripping whitespaces and standardizing title cases.
- **Outlier Detection:** Interquartile Range (IQR) technique for filtering extreme values in study hours.

### `1.3.ipynb` — Descriptive Statistics
- Custom algorithm implementation for central tendency measures:
  - Arithmetic Mean, Median, and Multi-modal detection.
- Sample Variance, Sample Standard Deviation, and Range computations.

### `1.4.ipynb` — Probability Distributions
- **Probability Mass Function (PMF):** Discrete distribution analysis for `Sleep_Hours`.
- **Probability Density Function (PDF):** Density histogram estimation for `Exam_Score`.
- **Cumulative Distribution Function (CDF):** Empirical cumulative distribution curve mapping.

### `1.5.ipynb` — Statistical Hypothesis Testing
- **Two-Sample Welch's t-Test:** Testing whether mean exam scores differ significantly across student genders ($H_0: \mu_{male} = \mu_{female}$).
- **Chi-Squared Test of Independence:** Evaluating association between `Gender` and `Internet_Access` ($\alpha = 0.05$).

### `1.6.ipynb` — Simple Linear Regression
- Analytical derivation of least-squares line ($y = mx + c$) from mathematical first principles.
- Calculation of slope ($m$) and intercept ($c$) between `Hours_Studied` and `Exam_Score`.
- Goodness-of-fit evaluation using $R^2$ (Coefficient of Determination) and regression scatter plotting.
- Interactive user prompt for exam score prediction based on study hours.

### `1.7.ipynb` — Exploratory Data Visualizations
- Univariate distributions with Histograms.
- Bivariate correlation checks with Scatter Plots.
- Categorical comparisons via Bar Charts and Composition Pie Charts.

---

## 🚀 Setup & Execution

### Prerequisites
- Python 3.8+
- Jupyter Notebook / Google Colab / JupyterLab

### Installation
Clone this repository and install the required dependencies:

```bash
git clone https://github.com/Anshikaa11/fds.git
cd fds
pip install -r requirements.txt
```

### Running the Notebooks
Launch Jupyter Notebook in your workspace:
```bash
jupyter notebook
```
Or upload any `.ipynb` file directly into [Google Colab](https://colab.research.google.com/).

---

## 🛠️ Tech Stack & Dependencies

- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Data Visualization:** `matplotlib`
- **Statistical Computing:** `scipy`
