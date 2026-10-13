
# 🧠 Autism Spectrum Disorder (ASD) Screening Data Analysis

Exploratory data analysis of toddler behavioral screening data using Python, focusing on Q-Chat-10 questionnaire responses, demographic attributes, and patterns associated with ASD screening classifications.

## 📌 Project Overview

This project explores a dataset designed for Autism Spectrum Disorder (ASD) screening in toddlers. It analyzes behavioral questionnaire responses and demographic attributes to identify patterns associated with the dataset's screening labels.

Using data cleaning, exploratory data analysis (EDA), and visualization, the project examines relationships among questionnaire scores, demographic characteristics, family history, and screening outcomes.

**Objective:** Demonstrate data preprocessing, exploratory analysis, and visualization techniques on a real-world behavioral screening dataset.

> **Disclaimer:** This project is for educational and analytical purposes only. Dataset classifications are screening labels, not independent clinical diagnoses. The findings do not establish causation or provide medical advice.

---

## 📂 Dataset Description

- **Dataset:** Toddler Autism dataset
- **Original source:** [ASDTests.com](http://www.asdtests.com/)
- **Author attribution:** Dr. Fadi Thabtah, as identified in the original project documentation
- **Format:** CSV
- **Reported instances:** 1,054
- **Reported attributes:** 18, including the class label
- **Questionnaire:** Q-Chat-10

### Feature Overview

| Feature | Description |
|---|---|
| `A1`–`A10` | Binary responses to Q-Chat-10 screening questions |
| `age` | Age of the toddler |
| `sex` | Recorded sex category |
| `ethnicity` | Recorded ethnic background |
| `jaundice` | Reported jaundice history at birth |
| `family_mem_with_ASD` | Family history of ASD |
| `who_completed_the_test` | Person completing the questionnaire |
| `class` | Dataset screening classification |

*Refer to the accompanying dataset description for the complete feature definitions and original coding conventions.*

### Data Quality and Leakage Considerations

- Examined dataset structure, column types, and data quality.
- Checked for duplicate records and removed duplicates where appropriate.
- Reviewed the `Score` variable and excluded it from potential predictive modeling because it was used to derive the target label, which could introduce **target leakage**.
- The original project documentation reports no missing values; this should be verified against the dataset during preprocessing.

---

## 🎯 Project Objectives

- Explore the distribution of behavioral screening responses.
- Investigate relationships between demographic attributes and screening classifications.
- Clean and preprocess data for reliable analysis.
- Visualize patterns involving gender, ethnicity, jaundice history, and family history.
- Identify potential directions for further statistical analysis and machine learning.

---

## 🔍 Analysis Performed

### 1. Data Exploration and Preprocessing

- Inspected dataset dimensions, column types, and categorical variables.
- Reviewed duplicate records and data consistency.
- Examined questionnaire features and the target classification.
- Considered target leakage when evaluating variables for potential predictive modeling.

### 2. Demographic Analysis

- **Ethnicity:** Compared screening-classification counts and proportions across recorded ethnic groups.
- **Gender:** Examined differences in screening classifications across recorded sex categories.
- **Jaundice history:** Explored the distribution of screening labels by reported jaundice history.
- **Family history:** Compared screening classifications for toddlers with and without a reported family history of ASD.

### 3. Data Visualization

Created visualizations to investigate:

- Screening-classification distribution.
- Gender-wise classification patterns.
- Ethnicity-wise classification counts.
- Associations between jaundice history and screening labels.
- Associations between family history and screening labels.

---

## 📊 Key Observations

The original analysis reported the following patterns in the dataset:

- White European participants had the highest number of classified ASD cases, while Pacifica participants had the highest reported proportion within their group.
- Male participants had a higher reported proportion of positive classifications.
- A slight association was observed between reported jaundice history and screening classification.
- A higher proportion of positive classifications was reported among toddlers with a family history of ASD.

These observations describe the analyzed sample only. Group sizes, possible confounding factors, and dataset composition should be considered before interpreting differences. They do not establish causation, clinical risk, or population-wide prevalence.

---

## 🛠️ Technology Stack

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Data Format:** CSV

*Confirm the libraries used in the notebook before finalizing this list.*

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- pip
- Jupyter Notebook

### 1. Clone the Repository

```bash
git clone https://github.com/dhruvii-web/ASD-Screening-Data-Analysis.git
cd ASD-Screening-Data-Analysis
```

### 2. Create a Virtual Environment

**Windows:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**Linux/macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Launch the Notebook

```bash
jupyter notebook autismdata.ipynb
```

Run the notebook cells in sequence to reproduce the analysis. Ensure the CSV dataset is available at the file path expected by the notebook.

---

## 🔮 Future Scope

- **Machine Learning:** Evaluate classifiers such as Logistic Regression, Random Forest, and Support Vector Machines.
- **Model Evaluation:** Report precision, recall, F1-score, confusion matrices, and suitable validation results.
- **Interpretability:** Explore feature importance or SHAP-based explanations for model predictions.
- **Robust Validation:** Use stratified validation and check for class imbalance and potential data leakage.
- **Interactive Dashboards:** Build an interactive interface for exploring dataset distributions and screening patterns.

These are proposed extensions and are not claimed as completed features.

---

## 📁 Repository Contents

- `README.md` — Project documentation.
- `Toddler Autism dataset July 2018.csv` — Screening dataset.
- `Toddler data description.docx` — Dataset documentation.
- `autismdata.ipynb` — Jupyter notebook containing the analysis.

---

## 📄 Data Source and Attribution

The dataset and original project documentation should be credited to their respective creators. Review the dataset's terms of use and redistribution conditions before sharing the data publicly.

**Repository:** [dhruvii-web/ASD-Screening-Data-Analysis](https://github.com/dhruvii-web/ASD-Screening-Data-Analysis)

