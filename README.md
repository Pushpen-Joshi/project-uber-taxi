# Modern Data Engineering Project 🚗[OnGoing]
End to end data pipeline project for Uber Taxi 🚕

## Objective

In this project, I designed and implemented an end-to-end data pipeline that consists of several stages:
1. Extracted data from NYC Trip Record Data website and loaded it into Google Cloud Storage for further processing.
3. Transformed and modeled the data using fact and dimensional data modeling concepts using Python on Jupyter Notebook.
4. Using ETL, orchestrated the data pipeline on Mage and loaded the transformed data into Google BigQuery.
5. Developed a dashboard on Looker Studio to generate insights.

Being a data engineering project, the emphasis is primarily on the engineering aspect with a lesser emphasis on analytics and dashboard development.

## Dataset

This project uses the TLC Trip Record Data which include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

More info about dataset can be found here:
- Website: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- Data Dictionary: https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf
- Raw Data: https://github.com/Pushpen-Joshi/project-uber-taxi/blob/aaa6055777dd9effc9cce8611e0f39b8e23d3de6/data/uber_data.csv

The following technologies are used to build this project:
- Language: [Python](https://www.python.org/), SQL
- Extraction and transformation: [Jupyter Notebook](https://jupyter.org/), [Google BigQuery](https://cloud.google.com/bigquery/)
- Storage: [Google Cloud Storage](https://cloud.google.com/storage)
- Orchestration: [Mage](https://www.mage.ai)
- Dashboard: [Looker Studio](https://lookerstudio.google.com)

## Data Pipeline Architecture
![image](https://github.com/Pushpen-Joshi/project-uber-taxi/assets/112235293/5089a0bf-152b-4710-90ee-7a7ea5c28b8c)

## Steps Involved

- Step 1: Cleaning and transformation: Following is the transformation code written in python to transform the data into desired state and test locally.
   [transformation-code.ipynb](https://github.com/Pushpen-Joshi/project-uber-taxi/blob/88822d0d464b11007d2e7776faf8f3124ab7ed1c/etl_pipeline.ipynb)
- Step 2: Storage:
   Load the data into google cloud storage bucket. Methods to upload data in a bucket can be found in below link.
   [Uploading objects in google cloud storage](https://cloud.google.com/storage/docs/uploading-objects)
- Step 2: ETL Orchestration - Mage 
   - [Data Loader](https://github.com/Pushpen-Joshi/project-uber-taxi/blob/88822d0d464b11007d2e7776faf8f3124ab7ed1c/Mage/uber-data-loader.ipynb):
      This code block fetches the data from google cloud storage bucket and ready the data for the next transfomation step. The output of this code block would be used as i       input for the next transformation block.
   - [Transform](https://github.com/Pushpen-Joshi/project-uber-taxi/blob/88822d0d464b11007d2e7776faf8f3124ab7ed1c/Mage/uber-data-transform.ipynb):
      This code block transforms the raw csv data into a fact and dimension tables model along with cleansing of data such as removing duplicates. The output of this transformation block would be used as input for the next data export block.
   - [Export](https://github.com/Pushpen-Joshi/project-uber-taxi/blob/88822d0d464b11007d2e7776faf8f3124ab7ed1c/Mage/uber-data-extract.ipynb):
      This code block uses the output of transform block as input and exports the data into Google BigQuery dataset for further analysis.

## Data Model

![image](https://github.com/Pushpen-Joshi/project-uber-taxi/assets/112235293/a1ea07d4-bad4-4908-b028-c2420b7fdfa6)


## Dashboard
Here is the Looker Studio Dashboard link: [Uber Dashboard](https://lookerstudio.google.com/reporting/e616a4f8-1793-4829-8c53-1eba26f496c5)


