# Data Engineering and AI Project

This project investigates whether patient data can be used to predict the presence of heart disease.

The project uses the **281K Patient Dataset for Multi-Disease Prediction** from Kaggle and follows a data engineering and machine learning pipeline covering data inspection, cleaning, analysis, feature engineering, modelling, and evaluation.

## Dataset

**Dataset:** 281K Patient Dataset for Multi-Disease Prediction
**Source:** Kaggle
https://www.kaggle.com/datasets/danishjmeo/281k-patient-dataset-for-multi-disease-prediction

Download the dataset and save it as:

```text
data/patient_data.csv
```

## Project Structure

```text
Data-Engineering-and-AI-Project/
|-- data/
|   `-- patient_data.csv
|-- notebooks/
|   |-- Task_2_Data_Acquisition_Inspection_and_Documentation.ipynb
|   |-- Task_3_Data_Cleansing_and_Transformation.ipynb
|   `-- Task_4_Exploratory_Data_Analysis_and_Visualisation.ipynb
|-- README.md
|-- DIRECTORY.md
`-- requirements.txt
```

## Setup

### 1. Clone the repository

```bash
git clone <repository-url>
cd Data-Engineering-and-AI-Project
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

### 3. Activate the virtual environment

**Windows:**

```bash
.venv\Scripts\activate
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Add the dataset

Download the dataset from Kaggle and place it at:

```text
data/patient_data.csv
```

### 6. Start Jupyter Notebook

```bash
jupyter notebook
```

Open the required notebook from the `notebooks/` folder.

## Phase 1

Phase 1 covers:

1. Problem Definition and Dataset Selection
2. Data Acquisition, Inspection, and Documentation
3. Data Cleansing and Transformation
4. Exploratory Data Analysis and Visualisation

## Requirements

* Python
* Jupyter Notebook
* Required Python packages are listed in `requirements.txt`
