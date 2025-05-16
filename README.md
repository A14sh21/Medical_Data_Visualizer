# Medical Data Visualizer

This Python project analyzes and visualizes patient data from medical examinations to explore relationships between cardiovascular disease and health indicators such as cholesterol, glucose, BMI, and lifestyle habits.

The project uses **Pandas**, **Seaborn**, and **Matplotlib** to produce:
- A **Categorical Plot** that compares good/bad health factors by heart disease diagnosis.
- A **Heatmap** that displays the correlation between numerical health variables.

---

##  Dataset

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+Disease)
- **Download**: [`medical_examination.csv`](https://raw.githubusercontent.com/freeCodeCamp/boilerplate-medical-data-visualizer/master/medical_examination.csv)

---

##  Features

| Feature         | Description                                       | Type               |
|-----------------|---------------------------------------------------|--------------------|
| age             | Age in days                                       | Integer            |
| height          | Height in cm                                      | Integer            |
| weight          | Weight in kg                                      | Float              |
| gender          | Gender code (1 or 2)                              | Categorical        |
| ap_hi           | Systolic blood pressure                           | Integer            |
| ap_lo           | Diastolic blood pressure                          | Integer            |
| cholesterol     | Cholesterol level (1=normal, 2=high, 3=very high) | Categorical        |
| gluc            | Glucose level (1=normal, 2=high, 3=very high)     | Categorical        |
| smoke           | Smoking status (0=no, 1=yes)                      | Binary             |
| alco            | Alcohol intake (0=no, 1=yes)                      | Binary             |
| active          | Physical activity (0=no, 1=yes)                   | Binary             |
| cardio          | Cardiovascular disease presence (0=no, 1=yes)     | Target Variable    |

---

##  Tasks Performed

###  Data Preprocessing
- Added overweight column based on BMI > 25.
- Normalized cholesterol and gluc to binary (0=good, 1=bad).
- Removed incorrect values:
  - ap_lo > ap_hi
  - Height & weight outside 2.5%–97.5% percentile range

###  Categorical Plot
Shows counts of:
- `cholesterol`, `gluc`, `smoke`, `alco`, `active`, `overweight`
- Split by heart disease diagnosis (`cardio=0` or `1`)

###  Heatmap
Displays correlation between:
- Age, height, weight, BMI, blood pressure, cholesterol, etc.

---

##  Technologies Used

- Python 3
- Pandas
- Seaborn
- Matplotlib
- Jupyter
