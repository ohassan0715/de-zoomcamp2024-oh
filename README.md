# Electric Vehicle Population 

## Overview
This repository contains the code for an Extract, Transform, Load (ETL) pipeline designed to process electric vehicle population data sourced from Kaggle and store it in Google Cloud Storage. The pipeline is orchestrated using Mage, a Workflow Orchestration tool, and executed within a Docker container. The data is subsequently loaded into Google BigQuery for analysis. The pipeline is scheduled to run monthly.

## Data Source
The data used in this pipeline is sourced from Kaggle and can be accessed [here](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population). It provides information about the population of electric vehicles.

## Pipeline Components
1) Data Extraction:
Python script (extract.py) retrieves data from the Kaggle API.
2) Data Transformation:
Data is transformed as necessary to prepare it for storage and analysis.
3) Data Loading:
Transformed data is loaded into Google Cloud Storage.
4) Batch Processing:
The pipeline is scheduled to run once a month to keep the data up to date.
5) Google Cloud Storage to BigQuery:
Python script (load_to_bigquery.py) utilizes PySpark to load data from Google Cloud Storage into BigQuery.
6) Terraform Configuration:
Terraform is used to manage Google Cloud Platform variables and credentials, facilitating quick setup for other users.

## Technologies Used
- Python
- Mage Workflow Orchestration
- Docker
- Google Cloud Storage
- Google BigQuery
- PySpark
- Terraform
- Tableau (for data visualization)

## Usage
1) Clone this repository:
git clone https://github.com/your-username/etl-electric-vehicles.git
2) Set up Terraform configurations for Google Cloud Platform variables and credentials.
3) Execute the Mage workflow to run the ETL pipeline within the Docker container.
4) Run the Python script (load_to_bigquery.py) to load data from Google Cloud Storage into BigQuery.
5) Visualize the data in Tableau for analysis and insights.

## Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
