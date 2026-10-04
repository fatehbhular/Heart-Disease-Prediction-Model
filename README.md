# ENGE707 Data Engineering and Machine Learning Project

This repository contains our Phase I and Phase II work on predicting heart disease from patient demographic, lifestyle, and clinical data.

The target column is `heart_disease_target`, where `0` means no heart disease and `1` means heart disease.

## What is included

- `notebooks Phase 1/` contains the data acquisition, cleaning, and exploratory analysis from Phase I.
- `notebooks Phase 2/` contains the eLCS experiments, preprocessing, model comparisons, statistical testing, and rule analysis from Phase II.
- `data/` contains the raw, cleaned, and feature-engineered datasets.
- `outputs/` contains the saved experiment results and report figures.
- `external/scikit-eLCS-master/` is the supplied scikit-eLCS 1.2.4 implementation used by the notebooks.
- The Phase I and Phase II reports are stored in the project root.

The main submission report is [Data Engineering and Machine Learning Pipeline Project Phase II.pdf](Data%20Engineering%20and%20Machine%20Learning%20Pipeline%20Project%20Phase%20II.pdf).

## Data

The original data comes from the [281K Patient Dataset for Multi-Disease Prediction](https://www.kaggle.com/datasets/danishjmeo/281k-patient-dataset-for-multi-disease-prediction).

The repository includes both the cleaned dataset and the feature-engineered datasets needed for the Phase II experiments:

- `data/patient_data.csv` - original patient data
- `data/patient_data_cleaned.csv` - cleaned Phase I data
- `data/X_train_preprocessed_full.csv` - full preprocessed training features
- `data/y_train_preprocessed_full.csv` - full training labels
- `data/X_train_preprocessed_undersampled.csv` - undersampled training features
- `data/y_train_preprocessed_undersampled.csv` - undersampled training labels
- `data/X_test_preprocessed.csv` - preprocessed test features
- `data/y_test_preprocessed.csv` - test labels

To reproduce the feature-engineered files, start with `patient_data_cleaned.csv` and run:

`notebooks Phase 2/Task_3_Data Cleansing and Transformation.ipynb`

This notebook creates the full training set, undersampled training set, and unchanged test set used by the later notebooks. To reproduce the cleaned dataset from the raw data, run the Phase I notebooks in order.

## Setup

Python 3.11 or newer is recommended.

On Windows:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --user --name enge707-phase2 --display-name "Python (ENGE707 Phase II)"
jupyter lab
```

On macOS or Linux, create and activate the environment with:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Then run the remaining `pip` and Jupyter commands shown above. Open the notebooks using the `Python (ENGE707 Phase II)` kernel.

## Notebook order

Phase I:

1. `notebooks Phase 1/Task_2_Data_Acquisition.ipynb`
2. `notebooks Phase 1/Task_3_Data Cleansing and Transformation.ipynb`
3. `notebooks Phase 1/Task_4_1_Exploratory_Data_Analysis.ipynb`
4. `notebooks Phase 1/Task_4_2_Exploratory_Data_Analysis.ipynb`

Phase II:

1. `notebooks Phase 2/Task_2_Original_eLCS_Baseline.ipynb`
2. `notebooks Phase 2/Task_3_Data Cleansing and Transformation.ipynb`
3. `notebooks Phase 2/Task_4_Improved_eLCS_System.ipynb`
4. `notebooks Phase 2/Task_5_Statistical_Testing.ipynb`
5. `notebooks Phase 2/Task_6_Compare_Models.ipynb`
6. `notebooks Phase 2/Task_7_XAI_Rule_Analysis.ipynb`

`notebooks Phase 2/Report_Figures.ipynb` creates the figures used in the report from the saved results.

## Results

The model notebooks can take a long time to run. Completed metrics, comparisons, rule exports, and figures are already available in `outputs/`, so the experiments do not need to be rerun just to review the project.
