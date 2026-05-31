# Porosity Regression from Well Logs

## Project Overview

This project demonstrates a supervised machine learning workflow to predict effective porosity (PHIE) from synthetic well log data.

The workflow is designed for geoscience and petroleum data science learning, with a focus on avoiding common modelling mistakes such as depth leakage.

## Business Context

Core porosity measurements are expensive and limited. Machine learning can help estimate porosity from commonly available wireline logs, supporting reservoir characterization, static modelling, and early field evaluation.

## Dataset

The project uses synthetic well log data generated inside the notebook to mimic realistic petrophysical relationships.

Main features include:

- Gamma Ray (GR)
- Bulk Density (RHOB)
- Neutron Porosity (NPHI)
- Sonic Log (DT)
- Resistivity (RT)
- Depth
- Well ID

Target:

- Effective Porosity (PHIE)

## Workflow

1. Generate synthetic well log data
2. Perform exploratory data analysis
3. Apply well-based train/validation/test split
4. Build a baseline model
5. Train regression models
6. Evaluate model performance
7. Analyze feature importance
8. Estimate uncertainty using P10–P90 prediction range
9. Save output data for future modules

## Models Used

- Ridge Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor

## Key Geoscience Lesson

Random row-based splitting can create depth leakage because nearby depth samples are highly correlated.  
This project uses well-based splitting to better simulate real-world model generalization to unseen wells.

## Repository Structure

```text
petromind-porosity-regression/
│
├── notebooks/
│   └── 01_Porosity_Regression.ipynb
│
├── data/
│   └── README.md
│
├── outputs/
│   └── README.md
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
