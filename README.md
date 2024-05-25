# ETL Pipeline Using Airflow and AWS EMR Cluster
I developed an ETL pipeline using Airflow that performs the following tasks: It downloads data from an AWS S3 bucket, triggers a remote Spark/Spark SQL job on an AWS EMR cluster to process the downloaded data, and generates a cleaned dataset highlighting orders missing delivery deadlines. This cleaned dataset is then uploaded back to the same S3 bucket, organized in a folder designed for advanced analytics.

# Problem Statement
Retailers in the current landscape are adapting to the digital age. Digital retail giants have carved out substantial market shares online, while traditional retail stores are generally in decline. In this era of digital transformation, adopting an omni-channel retail strategy is essential to stay competitive. This is particularly crucial for retailers with a large network of brick-and-mortar stores or those with strong ties to physical retail partners.

This data engineering project leverages a real-world retail dataset to analyze delivery performance on a large scale. The primary objective of the data engineering efforts in this project is to establish a robust foundation for data analytics and modelling, as well as to provide daily summary reports for decision-makers.

The project involves a series of ETL jobs programmed using Python, SQL, Airflow, and Spark. These pipelines download data from an AWS S3 bucket, perform various manipulations, and then upload the refined dataset to another location within the same AWS S3 bucket for advanced analytics.


# Dataset of Choice
The dataset chosen for this project consists of a series of tables provided by the Brazilian e-commerce company, Olist.


# Methodology
I developed an ETL pipeline using Airflow to load the required data and scripts into an S3 data lake. I then scheduled the DAG to run the script on the EMR cluster by adding job flow steps with the boto3 library. This setup successfully integrated AWS EMR into the pipeline, allowing the Spark job to run on a cluster rather than locally on a machine.
