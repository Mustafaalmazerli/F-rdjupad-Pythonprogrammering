🙌🙌😎
# f-rdjupad-pythonprogrammering
# Titanic Data Processing and SQL Storage
This project automates the process of reading, processing, and saving Titanic passenger data from the train.csv file to an SQL database. The system is built with Python and uses Pandas for data manipulation, SQLite for data storage, and unittest for automated testing.

# Features
 # Automated Data Pipeline: The program reads Titanic data from a CSV file, processes and formats it (e.g., handling missing values, converting data types), and stores the processed data in a local 
 SQLite database.
# Data Processing: Specific columns are selected from the Titanic dataset, and new columns (e.g., IsChild) are created to categorize passengers based on age.
# SQL Database Storage: The processed data is saved into an SQLite database, making it easy to query and analyze in the future.
# Error Handling & Logging: All errors during execution are logged to a file, making debugging easier.
# Automated Tests: The system includes unit tests to ensure that data reading, processing, and saving functionalities work as expected.



# Project Structure

   * F-rdjupad-Pythonprogrammering
   * read.py              # Reads Titanic data from CSV
   * process.py           # Processes and formats the Titanic data
   * save.py              # Saves the processed data into an SQLite database
   * main.py              # The main script to orchestrate the workflow
   * train.csv            # Titanic dataset (train.csv)
   * README.md            # Project documentation



# Requirements
  *  Python 3.x
  *  Libraries: pandas, sqlite3, unittest, schedule



# How to Run
 1: Run the main script:
 2: Download the project files.
    * run the following command in the terminal:
     python main.py.


# This will:

* Read Titanic data from train.csv.
* Process the data (handling missing values, type conversion, etc.).
* Save the processed data to an SQLite database.

# View the log file:

All actions are logged in a log file (titanic_data.log) located in the project directory. This log file will show if any errors occurred or if everything ran smoothly.


# Schedule Automated Execution:
You can schedule the main script to run at regular intervals (e.g., every day at a specific time) using the schedule library. The main.py script is already configured to run the job daily at 10:50.



# License
  * This project is open source and available under the MIT License.
