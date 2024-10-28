# Southern Water Corp Desalination Unit Failure Prediction

## Problem Statement

Southern Water Corporation (SW Corp) is facing a surge in demand for desalinated water. This has led to increased revenues, but also increased strain on their three desalination plants (Kootha, Surjek, and Jutik). To optimize operations and increase revenue further, SW Corp needs to:

1. **Resolve Budget Discrepancies:** Identify sizable discrepancies between actual and budgeted figures in the Cost to Produce (CTP) water.
2. **Analyze CTP Drivers:** Determine the key factors influencing the CTP and find areas for potential cost reduction.
3. **Predict Pump Failures:**  Develop a predictive model to anticipate pump failures in the Surjek plant, thereby reducing downtime and maintenance costs.

## Overview

This project analyzes time-series data from the Surjek desalination plant to identify cost discrepancies, key cost drivers, and predict pump failures using machine learning. The goal is to provide actionable insights to SW Corp for cost optimization and revenue enhancement.

## Installation

1. **Clone the Repository:** 
   ```bash
   git clone https://github.com/your_username/southern-water-corp-desalination.git
   cd southern-water-corp-desalination
   ```

2. **Create a Virtual Environment:** (Recommended)
   ```bash
   python -m venv env 
   source env/bin/activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Project Structure

```
southern-water-corp-desalination/
|- Desalination_Unit_File_001.csv
|- Desalination_Unit_File_002.csv
|- Desalination_Unit_File_003.csv
|- Problem Statement.docx 
|- Python_Southern_Water_Corp_Case_Study_BBDS.ipynb
|- README.md
|- requirements.txt 
```

## Files

* **Desalination_Unit_File_001.csv, 002.csv, 003.csv:**  Sensor data from the Surjek plant.
* **Problem Statement.docx:**  Detailed explanation of the business problem and context.
* **Python_Southern_Water_Corp_Case_Study_BBDS.ipynb:**  Jupyter Notebook containing the analysis and prediction model.
* **README.md:** This file.
* **requirements.txt:** List of Python libraries required for the project.


## Data

The CSV files contain time-series data from sensors within the Surjek desalination plant. 

**Features:**

* **SURJEK_FLOW_METER_1 & 2:** Flow rate readings from two sensors.
* **ROTATIONAL_PUMP_RPM:** Rotational speed of the pump.
* **SURJEK_PUMP_TORQUE:** Torque exerted by the pump.
* **MAXIMUM_DAILY_PUMP_TORQUE:**  Maximum torque value recorded for the day.
* **SURJEK_AMMONIA_FLOW_RATE:**  Flow rate of ammonia (used in the desalination process).
* **SURJEK_TUBE_PRESSURE:** Pressure within the desalination tubes. 
* **SURJEK_ESTIMATED_EFFICIENCY:** Estimated efficiency of the pump.
* **PUMP FAILURE (1 or 0):** Binary indicator of pump failure.
* **TIMEFRAME:** Timestamp of the recorded data.


## Methodology

The `Python_Southern_Water_Corp_Case_Study_BBDS.ipynb` Jupyter Notebook outlines the complete analysis process:

1. **Data Loading & Exploration:** Import the datasets, examine data types and distributions, and identify missing values.
2. **Data Cleaning & Preprocessing:** Handle missing values, perform feature scaling, and engineer new features if necessary.
3. **Exploratory Data Analysis:** Visualize relationships between variables, identify trends and patterns, and assess the impact of potential CTP drivers.
4. **Variance Analysis:** Compare actual and budgeted CTP figures, highlighting significant discrepancies and potential causes.
5. **Pump Failure Prediction:**
    * Split the data into training and testing sets.
    * Train a machine learning model (e.g., Logistic Regression, Random Forest, SVM) to predict pump failures based on sensor readings.
    * Evaluate model performance using relevant metrics (e.g., accuracy, precision, recall, F1-score).
6. **Recommendations:** Formulate actionable insights based on the analysis, suggesting measures to:
    * Reduce CTP by optimizing resource allocation or process adjustments.
    * Implement a pump failure prediction system for proactive maintenance.

## Results & Conclusions 

The notebook presents the findings of the analysis, including:

* Identified areas of budget discrepancies in the CTP.
* Key CTP drivers and their influence on costs.
* Performance evaluation of the pump failure prediction model.

The project aims to provide SW Corp with data-driven recommendations to optimize operations, reduce costs, and ultimately increase revenue. 

## How to Use

1. Follow the **Installation** steps above.
2. **Run the Notebook:** Execute each cell of the Jupyter Notebook in sequence.
3. **Review Results:** Examine the output of each step, including visualizations and model evaluation metrics.
4. **Adjust Parameters:**  The notebook may contain parameters you can modify (e.g., choice of model, hyperparameter tuning). Experiment to achieve optimal results. 
