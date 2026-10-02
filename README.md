# Multi-Disease Prediction — ENGE707

This project investigates whether patient demographic, lifestyle, and clinical information can predict the presence of heart disease.

The binary prediction target is `heart_disease_target`:

- `0` — no heart disease
- `1` — heart disease

## Dataset

**Dataset:** 281K Patient Dataset for Multi-Disease Prediction  
**Source:** Kaggle  
**Link:** https://www.kaggle.com/datasets/danishjmeo/281k-patient-dataset-for-multi-disease-prediction

The dataset combines patient information from diabetes, heart-disease, and hypertension datasets.

### Raw dataset

The raw dataset is stored at `data/patient_data.csv` and contains:

- 280,985 records
- 39 columns
- 2,284 exact duplicate records
- Approximately 2.1% positive heart-disease cases
- No missing values

### Cleaned Phase I dataset

The cleaned dataset is stored at `data/patient_data_cleaned.csv` and contains:

- 278,701 records
- 40 columns
- 272,810 class-0 records
- 5,891 class-1 records
- No exact duplicate records
- No missing values

The additional `heart_disease_target` column was created from `sublabel`. Values containing `HT` represent heart disease and are mapped to class 1; all other values are mapped to class 0.

## Project structure

```text
Multi_Disease_Prediction_ENGE707/
├── data/
│   ├── patient_data.csv
│   ├── patient_data_cleaned.csv
│   ├── X_train_preprocessed_full.csv
│   ├── y_train_preprocessed_full.csv
│   ├── X_train_preprocessed_undersampled.csv
│   ├── y_train_preprocessed_undersampled.csv
│   ├── X_test_preprocessed.csv
│   └── y_test_preprocessed.csv
├── notebooks/
│   ├── Task_2_Data_Acquisition.ipynb
│   ├── Task_3_Data Cleansing and Transformation.ipynb
│   ├── Task_4_1_Exploratory_Data_Analysis.ipynb
│   └── Task_4_2_Exploratory_Data_Analysis.ipynb
├── notebooks-phase2/
│   ├── Task_2_Original_eLCS_Baseline.ipynb
│   ├── Task_3_Data Cleansing and Transformation.ipynb
│   └── Task_4_Improved_eLCS_System.ipynb
├── external/
│   └── scikit-eLCS-master/
├── outputs/
├── requirements.txt
└── README.md
```

## Notebook execution order

### Phase I

1. `notebooks/Task_2_Data_Acquisition.ipynb`
2. `notebooks/Task_3_Data Cleansing and Transformation.ipynb`
3. `notebooks/Task_4_1_Exploratory_Data_Analysis.ipynb`
4. `notebooks/Task_4_2_Exploratory_Data_Analysis.ipynb`

### Phase II

1. `notebooks-phase2/Task_2_Original_eLCS_Baseline.ipynb`
2. `notebooks-phase2/Task_3_Data Cleansing and Transformation.ipynb`
3. `notebooks-phase2/Task_4_Improved_eLCS_System.ipynb`

Task 2 establishes the original raw-data eLCS baseline. Task 3 preprocesses the cleaned dataset and creates the full and undersampled training datasets. Task 4 compares the original preprocessed eLCS, undersampling-only eLCS, and final improved eLCS.
