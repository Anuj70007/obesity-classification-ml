#  Obesity Classification using Machine Learning

##  Overview
This project predicts **obesity levels** (such as Normal Weight, Overweight, Obesity Types I–III, etc.) using various **machine learning models** — **Random Forest**, **XGBoost**, and **Decision Tree**.  
It performs full **data preprocessing**, **exploratory data analysis (EDA)**, and **model comparison** to identify the best-performing classifier.

---

## Project Structure
obesity-classification-ml/
│
├── obesity_classification.ipynb ← Main notebook
├── datasetnew/ ← Folder containing datasets
│ ├── train.csv
│ ├── test.csv
│ ├── sample_submission.csv
│ └── ObesityDataSet.csv
└── final_submission.csv ← Model predictions (output)'


---

##  Dataset
The dataset contains health and lifestyle attributes like:
- Gender, Age, Height, Weight  
- Family history with overweight  
- Daily habits: food intake, water consumption, physical activity  
- Target variable: `WeightCategory` (7 classes)

All CSVs used are stored in the `datasetnew/` folder for easy access.

---

## ⚙️ Steps Performed
1. **Data Loading and Cleaning**  
   - Reads CSVs from `/datasetnew/`  
   - Handles missing values  
   - Separates numerical and categorical features

2. **Exploratory Data Analysis (EDA)**  
   - Prints dataset info and summary statistics  
   - Displays target distribution and feature histograms  
   - Shows feature correlation matrix  

3. **Model Building**  
   - Three models used:
     -  Random Forest  
     -  XGBoost (main performing model)  
     -  Decision Tree  
   - Preprocessing done with sklearn pipelines

4. **Cross-Validation**  
   - 5-fold stratified CV  
   - Metric used: **F1 Macro**

5. **Final Training & Prediction**  
   - Best model selected (XGBoost achieved best results)  
   - Final predictions saved as `final_submission.csv`

---

##  Results

| Model | Mean F1 (5-fold CV) | Validation F1 |
|--------|---------------------|----------------|
| Random Forest | 0.8966 | - |
| XGBoost | **0.9076** | **0.9172** |
| Decision Tree | 0.89 (approx) | - |

**Kaggle Public Score:** `0.91377`

---

##  How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/<your-username>/obesity-classification-ml.git
   cd obesity-classification-ml
2. Open in Jupyter Notebook or Kaggle:
   jupyter notebook obesity_classification.ipynb
3.Ensure all datasets are placed inside the datasetnew/ folder.
4.Run all cells — results and visualizations will be generated automatically.

## Tech Stack
Language: Python 3.11+
Libraries:
  - NumPy
  - Pandas
  - Matplotlib
  - Scikit-learn
  - XGBoost
IDE:
  - Kaggle
  - Jupyter Notebook

## Key learnings
- Using F1-Macro for balanced evaluation across classes
- Comparing ensemble models like Random Forest and XGBoost
- Importance of consistent preprocessing and encoding
- Gaining insights into lifestyle patterns linked to obesity


