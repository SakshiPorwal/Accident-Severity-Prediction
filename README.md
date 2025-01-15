# Road Accidents Analysis and Prediction

## Overview
This project analyzes and predicts accident severity using the US Accidents dataset. It involves data cleaning, feature engineering, exploratory data analysis (EDA), and machine learning model development to provide insights into accident severity and contributing factors. The ultimate goal is to contribute to improved road safety by making data-driven recommendations.

---

## Dataset
### Source:
- **Name:** US Accidents Dataset
- **Link:** [Download Dataset](https://drive.google.com/file/d/1edKrdWNOcgbAo2JtckX-PEyM0FdEq4EG/view?usp=drive_link)

### Description:
The dataset contains records of traffic accidents in the United States, with attributes describing accident details, weather conditions, location, and environmental factors.

### Key Features:
| Attribute          | Description                                                   | Nullable |
|--------------------|---------------------------------------------------------------|----------|
| `ID`              | Unique identifier of the accident record                      | No       |
| `Severity`        | Severity of the accident (1 to 4)                             | No       |
| `Start_Time`      | Accident start time                                           | No       |
| `End_Time`        | Accident end time                                             | No       |
| `Distance(mi)`    | Length of the road extent affected                            | No       |
| `Weather_Condition`| Weather conditions during the accident                        | Yes      |
| ...               | Additional features such as location, POI annotations, etc.   | Yes      |

---

## Objectives
1. **Data Cleaning & Preparation:**
   - Handle missing values.
   - Standardize date formats.
   - Engineer new features for model enhancement.
2. **Exploratory Data Analysis:**
   - Identify patterns and trends in accident data.
   - Conduct geospatial and temporal analyses.
3. **Machine Learning:**
   - Build and validate a model to predict accident severity.
   - Evaluate model performance using appropriate metrics.
4. **Recommendations:**
   - Provide actionable insights for improving road safety.

---

## Steps

### 1. Data Preparation
- Loaded the dataset into a Pandas DataFrame.
- Converted `Start_Time` and `End_Time` to datetime format.
- Created derived features such as:
  - `Duration` (in minutes).
  - Time-based features: `Hour`, `DayOfWeek`, `Month`.
- Handled missing values using imputation strategies.

### 2. Exploratory Data Analysis (EDA)
- **Severity Distribution:** Visualized the distribution of accident severity.
- **Geospatial Analysis:** Plotted accidents on a map using GPS coordinates.
- **Weather Analysis:** Identified the relationship between weather conditions and accident severity.
- **Time Analysis:** Explored patterns based on the time of day and day of the week.

### 3. Model Building
- **Target Variable:** Severity (`1` to `4`).
- **Features Selected:**
  - `Distance(mi)`, `Temperature(F)`, `Humidity(%)`, `Pressure(in)`, `Visibility(mi)`, `Wind_Speed(mph)`, `Hour`, `DayOfWeek`.
- **Data Split:**
  - Training set: 75%
  - Validation set: 15%
  - Test set: 10%
- **Algorithms Used:**
  - Random Forest Classifier (selected for interpretability and accuracy).
  - Logistic Regression (baseline model).
- **Evaluation Metrics:**
  - Accuracy, Precision, Recall, F1-Score.
  - Confusion Matrix and AUC-ROC.

### 4. Recommendations
- **Insights:**
  - Higher accident severity is often correlated with adverse weather conditions, poor visibility, and nighttime accidents.
  - Accidents tend to cluster around urban areas and during peak traffic hours.
- **Recommendations:**
  - Improve infrastructure in high-severity zones.
  - Enhance lighting and visibility in high-risk areas.
  - Use real-time weather data to warn drivers during adverse conditions.

---

## Deliverables
1. **Jupyter Notebook:**
   - Includes data cleaning, EDA, and machine learning steps.
2. **Trained ML Model:**
   - Predicts accident severity with validation metrics.
3. **Recommendations Report:**
   - Data-driven strategies for accident mitigation.

---

## Tools & Technologies
- **Programming Language:** Python
- **Libraries:**
  - `pandas`, `numpy` (data manipulation)
  - `matplotlib`, `seaborn`, `plotly` (visualization)
  - `scikit-learn` (machine learning)
- **Environment:** Jupyter Notebook

---

## How to Run the Project
1. Clone this repository.
2. Install required Python libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Download the dataset and place it in the project directory.
4. Run the Jupyter Notebook step by step.

---

## Future Work
- Integrate real-time accident data for live predictions.
- Explore deep learning models for better performance.
- Deploy the model as an API or web app.

---

## Contact
For any questions or collaborations, please reach out:
- **Email:** sakshiporwal2002@gmail.com
- **LinkedIn:** [Your LinkedIn Profile](https://linkedin.com/in/sakshiporwal)

---

### Acknowledgements
We acknowledge the source of the US Accidents dataset and contributors to the open data community for enabling this project.

