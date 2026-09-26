Drug200: Analyzing Prescription Patterns Based on Patient Characteristics
📌 Overview

This notebook analyzes the relationship between patient characteristics (age, sex, blood pressure, cholesterol, and sodium-to-potassium ratio) and the type of drug prescribed, using the drug200.csv dataset.

🎯 Goal

Understand prescribing patterns based on patient characteristics, in order to see which drugs tend to be given under which patient conditions.

📊 Data Source
File: drug200.csv
Source: Public "Drug Classification" dataset by Pratham Tripathi, available on Kaggle
Size: 200 patient records, 6 columns
Column	Description
Age	Patient's age
Sex	Gender (M/F)
BP	Blood pressure (LOW/NORMAL/HIGH)
Cholesterol	Cholesterol level (NORMAL/HIGH)
Na_to_K	Sodium-to-potassium ratio in blood
Drug	Prescribed drug (target/response variable) — DrugA, DrugB, DrugC, DrugX, DrugY
🗂️ Notebook Structure
Import and Inspect the Data — load the data, check shape, dtypes, and descriptive statistics
Data Cleaning — check for duplicates, missing values, and consistency in categorical labels (e.g. standardizing capitalization in the Drug column)
Exploratory Data Analysis (EDA) — distribution of age, Na_to_K ratio, and patient count per drug
Relationship Analysis Between Variables — analyzing how Na_to_K, age, BP, and cholesterol relate to drug choice
Interactive Visualizations with Plotly — all charts are interactive (hover, zoom, filter via legend)
Conclusion & Insights — summary of key findings
🔍 Key Insights
Patients with a Na_to_K ratio above ~15 tend to be prescribed DrugY, regardless of age.
DrugA is exclusively prescribed to patients aged ≤ 50 (median 36), while DrugB is exclusively prescribed to patients aged ≥ 51 (median 60) — the two age ranges never overlap.
DrugA and DrugB are prescribed exclusively to patients with high BP; DrugC exclusively to low BP; DrugX never appears in high-BP patients; only DrugY appears across all BP levels.
DrugC is the only drug never prescribed to patients with normal cholesterol, suggesting it may be specifically indicated for high-cholesterol cases. DrugY is consistently prescribed across both cholesterol levels.
⚠️ Limitations

This dataset is small (200 rows) and synthetic/educational, so the patterns found here should not be generalized to a real patient population without further validation.

🛠️ Tools & Libraries
Python 3
Jupyter Notebook
pandas — data loading and manipulation
numpy — numerical operations
plotly.express — interactive data visualization
🚀 How to Run
Make sure Python 3 and the following libraries are installed:
bash
   pip install pandas numpy plotly jupyter
Place the drug200.csv file in the same folder as the notebook.
Run:
bash
   jupyter notebook drugPortofolio.ipynb
Run all cells in order from top to bottom.
