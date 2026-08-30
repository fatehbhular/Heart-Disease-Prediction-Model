# Data Engineering and AI Project

This project investigates whether patient data can be used to predict the presence of heart disease.

Phase 1 focuses on data acquisition, inspection, cleaning, transformation and exploratory data analysis. Machine learning modelling is not included in this phase.

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
`-- README.md
```

## Notebook Execution Order

Run the notebooks in this order:

1. `Task_2_Data_Acquisition.ipynb`
2. `Task_3_Data Cleansing and Transformation.ipynb`
3. `Task_4_1_Exploratory_Data_Analysis.ipynb`
4. `Task_4_2_Exploratory_Data_Analysis.ipynb`

Task 3 cleans and validates the raw data, then stores the cleaned result in both `data/patient_data_cleaned.csv` and the `clean` table in `data/etl.db`.

Both Task 4 notebooks continue the exploratory analysis by loading `data/patient_data_cleaned.csv`.
