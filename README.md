# modern-data-engineering-project 🚗
End to end data pipeline proeject for Uber Taxi 🚕

## Objective

In this project, I designed and implemented an end-to-end data pipeline that consists of several stages:
1. Extracted data from NYC Trip Record Data website and loaded it into Google Cloud Storage for further processing.
3. Transformed and modeled the data using fact and dimensional data modeling concepts using Python on Jupyter Notebook.
4. Using ETL, I orchestrated the data pipeline on Mage and loaded the transformed data into Google BigQuery.
5. Developed a dashboard on Looker Studio.

As this is a data engineering project, the emphasis is primarily on the engineering aspect with a lesser emphasis on analytics and dashboard development.

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
