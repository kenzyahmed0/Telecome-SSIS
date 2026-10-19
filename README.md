# Telecom Data Warehouse – SSIS ETL Project

## Project Overview

This project implements an ETL workflow for a Telecom Data Warehouse case study using SQL Server Integration Services (SSIS) and Microsoft SQL Server.

The objective is to process telecom transaction data from CSV files, enrich the data using subscriber reference information, transform IMEI values, and load the processed data into database destinations.

## Technologies Used

- Microsoft SQL Server
- SQL Server Integration Services (SSIS)
- Visual Studio
- SQL
- CSV Files

## ETL Workflow

The SSIS Data Flow includes the following components:

1. Flat File Source: Reads telecom transaction data from CSV files.
2. Lookup Transformation – `LKP subscriber_id`: Matches IMSI values against the subscriber reference data to retrieve the corresponding subscriber ID.
3. Derived Column – `DER get subscriber_id`: Creates or derives the subscriber ID field based on the lookup results.
4. Derived Column – `DER calculate SNR & TAC`: Transforms IMEI values to derive TAC and SNR according to the case study requirements.
5. ADO.NET Destination: Loads processed data into the target database.
6. ADO.NET Destination Error Output: Redirects data-loading errors for further handling.
7. OLE DB Destination: Provides an additional database destination within the ETL workflow.

## Key Concepts Practiced

- Building SSIS Data Flow pipelines.
- Reading structured data from flat files.
- Performing Lookup transformations using reference data.
- Applying data transformations through Derived Column components.
- Configuring database destinations and column mappings.
- Working with error outputs and troubleshooting data-loading issues.
- Integrating CSV data with SQL Server databases.

## Project Scope

This implementation focuses on extracting, transforming, and loading telecom transaction data using SSIS. The case study also specifies additional requirements, including comprehensive record validation, rejected-record storage with source filename tracking, and archiving processed files. These requirements are not all implemented in the current version.

## Author

Kenzy Ahmed Fathy

Computer Science & Artificial Intelligence Student

GitHub: [kenzyahmed0](https://github.com/kenzyahmed0)
