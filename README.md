# Data Engineering and AI Project

This project investigates whether patient data can be used to predict the presence of heart disease.

Phase I focuses on data acquisition, inspection, cleaning, transformation and exploratory data analysis.

## Dataset

**Dataset:** 281K Patient Dataset for Multi-Disease Prediction  
**Source:** Kaggle  
**Link:** https://www.kaggle.com/datasets/danishjmeo/281k-patient-dataset-for-multi-disease-prediction

The raw dataset contains 280,985 records and 39 columns.

## Project Structure

```text
Data-Engineering-and-AI-Project/
|-- data/
|   |-- patient_data.csv
|   |-- patient_data_cleaned.csv
|   `-- etl.db
|-- notebooks/
|   |-- Task_2_Data_Acquisition.ipynb
|   |-- Task_3_Data Cleansing and Transformation.ipynb
|   |-- Task_4_1_Exploratory_Data_Analysis.ipynb
|   `-- Task_4_2_Exploratory_Data_Analysis.ipynb
|-- Data Engineering and Machine Learning Pipeline Project.pdf
|-- requirements.txt
`-- README.md
```

The cleaned dataset is stored in both `data/patient_data_cleaned.csv` and the
`clean` table in `data/etl.db`. The exploratory analysis notebooks continue to
load the cleaned CSV file.

## Setup

```powershell
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```
