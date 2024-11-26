# Healthcare Data Pipeline

This repository implements a healthcare data pipeline that processes and analyzes datasets related to patient demographics, symptoms, medications, and encounters. The pipeline cleans, structures, and analyzes the data to provide insights into patient information, medication trends, and symptom analysis. The project also includes a series of data transformations and analysis steps to ensure high-quality, actionable data.

# Project Structure

healthcare_pipeline/
│
├── data/                             # Raw data files
│   ├── patients.csv                 # Patient demographic data
│   ├── symptoms.csv                 # Symptoms data
│   ├── medications.csv              # Medications data
│   ├── conditions.csv               # Conditions data
│   ├── encounters.parquet           # Encounter data (in Parquet format)
│   └── gender.csv                   # Gender data (separate dataset)
│
├── notebooks/                        # Jupyter Notebooks for exploratory analysis
│   └── exploratory_analysis.ipynb    # Notebook for exploratory data analysis
│
├── src/                              # Source code for the pipeline
│   ├── healthcare_pipeline/         # Main pipeline module
│   │   ├── __init__.py              # Initialization for the module
│   │   ├── nodes/                   # Pipeline steps (e.g., cleaning, merging)
│   │   │   ├── cleaning.py          # Data cleaning steps
│   │   │   ├── analysis.py          # Contains code for Task 3 analysis
│   │   │   └── merging.py           # Data merging logic
│   │   └── pipeline.py              # Main pipeline definition
│
├── conf/                             # Configuration files
│   ├── base/                         # Base configurations
│   │   ├── catalog.yml               # Data catalog for data source definitions
│   │   ├── parameters.yml            # Pipeline parameters
│   │   └── credentials.yml           # Credentials for database access
│
├── tests/                            # Unit tests
│   └── test_pipeline.py              # Unit tests for pipeline functionality
│
├── README.md                         # Project overview and instructions
├── requirements.txt                  # Python dependencies
└── setup.py                           # Setup script for packaging the pipeline


# Project Overview

This project focuses on healthcare data management, patient demographic information, medication records, symptoms, and other clinical data. The pipeline is designed to:

1. Ingest data from multiple sources such as CSV and Parquet files.
2. Clean the data by addressing missing values, fixing data quality issues, and standardizing formats.
3. Structure the data into standardized columns as per the Tuva Data Model Input Layer.
4. Analyze the data to uncover insights, such as medication trends, racial distribution of patients, and symptom severity.
5. Merge datasets to create a master table for reporting and further analysis.

## The main tasks in this pipeline include:

1. Data Cleaning: Removing duplicates, fixing inconsistencies, and handling missing data.
2. Data Structuring: Mapping raw data to a standardized format based on the Tuva Data Model.
3. Analysis: Analyzing patient demographics, medication trends, and symptoms over time.


# Installation

To run the pipeline, clone this repository and install the necessary dependencies:

git clone https://github.com/username/healthcare_pipeline.git
cd healthcare_pipeline
pip install -r requirements.txt

# Running the Pipeline

To run the pipeline, use the following steps:

1.Prepare the data:

*. The raw data files (CSV/Parquet) are available in the data/ directory.

2.Run the pipeline:

Execute the pipeline script to process the data:



python src/healthcare_pipeline/pipeline.py

3.Explore the analysis:

Check the notebooks/exploratory_analysis.ipynb for an exploratory data analysis that visualizes patient demographics and other metrics.

# Testing
Unit tests for the pipeline logic are located in the tests/ directory. To run tests, use the following:

bash
Copy code
pytest tests/test_pipeline.py





