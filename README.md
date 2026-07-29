Install Dependencies:

Bash
pip install pandas numpy matplotlib seaborn scikit-learn
Place Dataset:
Ensure creditcard.csv is placed in the project root directory.

Launch Jupyter Notebook:

Bash
jupyter notebook
Open the main notebook file and run cells sequentially.

🤝 Developed for research and practical application in financial fraud analytics.
"""

with open("README.md", "w", encoding="utf-8") as f:
f.write(readme_english_content)

print("English README.md updated successfully!")


```text?code_stdout&code_event_index=1
English README.md updated successfully!

Your Markdown file is ready

README
 MD 
فتح

📝 English README.md Content:
Markdown
# 💳 Credit Card Fraud Detection Project

A Machine Learning and Data Science project focused on **Credit Card Fraud Detection** using advanced data resampling, exploratory data analysis, and multiple classification algorithms.

---

## 📌 1. Project Overview
The primary objective of this project is to address the severe **Class Imbalance** problem inherent in credit card transaction datasets. By constructing robust Machine Learning models, the system effectively predicts fraudulent activities, helping protect consumers and financial institutions from financial loss.

The project utilizes a **controlled resampling technique (Downsampling)** to build a representative dataset while testing and tuning various ML classifiers.

---

## 📊 2. Dataset & Reshaping Strategy
- **Original Source**: `creditcard.csv` (contains credit card transactions with PCA-transformed features `V1` through `V28`, along with `Time`, `Amount`, and the target variable `Class`).
- **Reshaping & Sampling Strategy**:
  - **Target Sample Size**: 15,000 records.
  - **Fraud Ratio**: Fixed at 3% (450 fraud transactions vs. 14,550 non-fraud transactions).
  - **Shuffle & Reproducibility**: Merged and randomly shuffled with a fixed `random_state = 42` to ensure consistent experiment repetition.

---

## 🔍 3. Data Exploration & Cleaning
A comprehensive exploratory data analysis (EDA) pipeline was conducted:
- **Dimensions Verification**: Final sampled dataset shape `(15000, 31)`.
- **Missing Values Check**: Zero missing values detected across all attributes (`df.isnull().sum() == 0`).
- **Duplicates Handling**: Identified and removed 20 duplicate rows to prevent data leakage and overfitting.
- **Descriptive Statistics**: Summary statistics (mean, std, min, max, quantiles) generated for feature understanding.

---

## 🛠️ 4. Tech Stack & Libraries

| Category | Libraries / Tools Used |
| :--- | :--- |
| **Data Manipulation** | `pandas`, `numpy` |
| **Data Visualization** | `matplotlib`, `seaborn` |
| **Preprocessing & Splitting** | `sklearn.preprocessing.StandardScaler`, `sklearn.model_selection.train_test_split` |
| **Classification Models** | `LogisticRegression`, `KNeighborsClassifier`, `SVC`, `DecisionTreeClassifier`, `RandomForestClassifier`, `ExtraTreesClassifier` |
| **Hyperparameter Tuning** | `GridSearchCV` |
| **Evaluation Metrics** | `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, `roc_auc_score`, `confusion_matrix`, `classification_report`, `RocCurveDisplay` |

---

## 📈 5. Project Workflow
1. **Environment Setup & Library Import**: Loading required Python packages.
2. **Data Ingestion & Reshaping**: Subsampling positive/negative classes to maintain target proportion.
3. **Data Inspection & Cleaning**: Checking missing data, duplicate removal, and summary metrics.
4. **Exploratory Data Analysis (EDA)**: Visualizing feature distributions and correlations.
5. **Feature Scaling & Train-Test Split**: Standardizing numerical features and splitting into 80/20 train/test sets.
6. **Model Training & Evaluation**: Training baseline classifiers and comparing benchmark scores.
7. **Hyperparameter Tuning**: Fine-tuning best-performing algorithms using `GridSearchCV`.

---

## 🚀 6. How to Run
1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd credit-card-fraud-detection
Install Dependencies:

Bash
pip install pandas numpy matplotlib seaborn scikit-learn
Place Dataset:
Ensure creditcard.csv is placed in the project root directory.

Launch Jupyter Notebook:

Bash
jupyter notebook
Open the main notebook file and run cells sequentially.

🤝 Developed for research and practical application in financial fraud analytics.
