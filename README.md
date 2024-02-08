# ETL-Pipeline-for-Multi-format-Data-Integration
# ETL Pipeline Documentation

## Overview
This documentation provides an overview and explanation of an Extract, Transform, Load (ETL) pipeline implemented in Python. The ETL pipeline is designed to process various types of data files (CSV, JSON, XML), extract relevant information, transform the data, and load it into a CSV file. The pipeline consists of several functions organized into logical steps: Extraction, Transformation, and Loading.

## Contents
1. Introduction
2. Components
3. Functionality
4. Usage
5. Dependencies

## 1. Introduction
This ETL pipeline automates the process of extracting data from multiple file formats (CSV, JSON, XML), transforming the extracted data by converting units (inches to meters, pounds to kilograms), and finally loading the transformed data into a CSV file. The pipeline is designed to handle large volumes of data efficiently and accurately.

## 2. Components
The ETL pipeline consists of the following components:

- **Extraction Functions**:
  - `extract_from_csv`: Extracts data from CSV files using Pandas.
  - `extract_from_json`: Extracts data from JSON files using Pandas.
  - `extract_from_xml`: Extracts data from XML files using ElementTree.

- **Extraction**:
  - `extract`: Combines extraction functions to extract data from all available CSV, JSON, and XML files in the current directory.

- **Transformation**:
  - `transform`: Converts height from inches to meters and weight from pounds to kilograms.

- **Loading**:
  - `load_data`: Saves the transformed data into a CSV file.

- **Logging**:
  - `log_progress`: Logs the progress of the ETL process into a log file.

## 3. Functionality
- **Extraction**:
  - The `extract` function iterates through all available CSV, JSON, and XML files in the current directory.
  - It utilizes specific extraction functions for each file type to extract data.
  - Extracted data is stored in a Pandas DataFrame.

- **Transformation**:
  - The `transform` function converts height from inches to meters and weight from pounds to kilograms.
  - The transformations are applied to the entire dataset.

- **Loading**:
  - The `load_data` function saves the transformed data into a CSV file specified by the user.

- **Logging**:
  - Progress of the ETL process is logged using the `log_progress` function.
  - Logs include timestamps and messages indicating the start and end of each phase (Extract, Transform, Load) and the overall ETL job.

## 4. Usage
To use the ETL pipeline:
1. Ensure the Python script containing the ETL functions is in the same directory as the data files.
2. Update the `log_file` and `target_file` variables to specify the log file path and target CSV file path.
3. Run the Python script.

## 5. Dependencies
The ETL pipeline relies on the following Python libraries:
- `pandas`: Used for data manipulation and processing.
- `xml.etree.ElementTree`: Used for XML parsing.
- `glob`: Used for file path pattern matching.
- `datetime`: Used for timestamp generation.

Ensure these libraries are installed in your Python environment to execute the ETL pipeline successfully.

This concludes the documentation of the ETL pipeline. For further inquiries or assistance, please contact the developer.
