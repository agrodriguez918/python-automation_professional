# python-automation_professional
This repository contains several professional projects designed by me. Projects are separated by title. 

# Project 1 : Healthcare File Read & Write Automation

This python script can be located in this repository under the name "python_file_read_prep.py"

# Overview

This project is a python based automation tool designed to streamline the processing of electronic health record (EHR) attestation documents and associated encounter data files. 

The tool accepts a user specified date, traverses a cloud based organizational file structure to locate matching folders, extracts structured information from PDF attestation documents, and updates
corresponding CSV files. It also maintains a historical Excel tracker to support encounter record keeping and downstream file submission workflows. 

The application incorporates date standardization and a dry-run mode to support consistent data processing and allow users to preview intended operations before making file changes.

This project demonstrates the application of python automation to complex healthcare data workflows involving document extraction, file system navigation, data transformation, and structural record management.

# Key Features

- Date Driven File Discovery : Accepts a target date in MM-DD-YYYY format and traverses a cloud-based folder hierarchy to identify folders associated with that date.
- PDF Table Extraction : Extracts structured information from PDF attestation documents for downstream processing.
- Date Standardization : Normalizes date values pulled from PDF attestations as well as rewrites unformatted dates in the .csv attestation to maintain consistency across processed records and output files.
- Automated CSV Updates : Replaces the contents of the corresponding attestation CSV files with processed information.
- Historical Recordkeeping : Appends processed records to an Excel (.xlsx) tracker to maintain a historical record of encounter data.
- Dry-Run Mode : Allows users to preview planned processing operations before committing file changes.
- Error Handline : Treats missing or unreadable required files as error rather than silently proceeding with incomplete processing.
- Workflow Integration : Supports the preparation and organization of encounter records for downstream healthcare file submission processes.

# Workflow

The automation follows a date driven processing workflow: 

1. User Input : The user enters the target date in MM-DD-YYYY format.
2. Folder Traversal : The script navigates the designated cloud based directory structure to locate folders associated with the specified date.
3. Document Identification : The script locates the required PDF attestation documents and corresponding CSV files within the matching folders.
4. Data Extraction : Structured information is extracted from the PDF and CSV documents.
5. Data Standardization : Date fields are standardized before the processed information is written to output files.
6. CSV Processing : The corresponding attestation CSV contents are replaced with the newly processed information.
7. Historical Tracking : Processed encounter information is appended to the historical Excel tracker.
8. Validation and Error Handling : Missing or unreadable required files are handled as errors.
9. Dry Run Review : When enabled, dry run mode allows the user to review planned operations before file modifications are performed.

# Technologies

- Python
- PDF table extraction
- CSV data processing
- Excel workbook manipulation
- Date parsing and standardization
- File system traversal
- Cloud synchronized directory navigation
- Input validation and error handling

The exact python libraries and dependencies can be viewed within the script. 

# Technical Challenges

- Navigating Complex Folder Structures : A central component of the tool is traversing a cloud based organizational file hierarchy to locate all folders corresponding to a user specified date. This reduces the need for users to manually locate and process individual encounter folders.

- Maintaining Consistent Date Formats : Date values may appear in different formats across source documents and output files. The script standardizes dates before writing the processed information, helping maintain consistency across records.

- Coordinating Multiple File Formats : The workflow connects PDF extraction, CSV updates, and Excel-based historical tracking. Each format serves a different purpose within the broader document processing and encounter recordkeeping process.

- Protecting Existing Records : The tool distinguishes between replacing the current attestation CSV and appending records to the historical tracker. These different write behaviors support the intended output structure for each file.

- Supporting Safer Execution : Dry-run functionality provides a way to inspect planned operations before changes are made. Error handling also helps prevent required missing or unreadable files from being silently overlooked.

# Professional Application 

This project originated from a professional healthcare data workflow involving EHR attestation documents and encounter records.

It demonstrates how Python can be used to automate document processing, navigate complex file structures, standardize data, and coordinate multiple output formats in support of operational healthcare processes.

The public repository contains only code and documentation approved for release. Employer-specific paths, internal file structures, credentials, proprietary business rules, confidential documents, and protected health information have been excluded.

