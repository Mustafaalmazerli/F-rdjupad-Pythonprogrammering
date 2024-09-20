# F-rdjupad-Pythonprogrammering

# Titanic Data Processing and SQL Storage
This project processes the Titanic dataset (from the train.csv file) by reading, transforming, and storing the data in an SQLite database. The script is designed to run automatically, handle exceptions, and includes unit tests to ensure the correctness of the processing. The key functionalities include automatic scheduling, data type conversion, and database updates.

Table of Contents
Project Overview
Prerequisites
Installation
Usage
Files
Testing
Logging
Future Improvements
Project Overview
The project focuses on automating the process of reading Titanic data, transforming key fields, and saving the result into a SQLite database. The key steps are:

Read Titanic data: The dataset is read from a CSV file.
Process data: Age and Fare columns are converted to appropriate data types, missing values in the Age column are filled with the median, and a new column IsChild is created to mark passengers under 18 years old.
Save data to SQL: The processed data is stored in an SQLite database for future analysis.
Automatic execution: The entire process is scheduled to run automatically at a specific time each day.
Logging and Exception Handling: The script logs all operations and captures any errors that occur.
Prerequisites
Before you begin, ensure you have met the following requirements:

Python 3.x installed on your machine.
Libraries: pandas, sqlite3, schedule, unittest.
Titanic train.csv dataset available.
To install the necessary Python libraries, run:

bash
Kopiera kod
pip install pandas schedule
Installation
Clone this repository to your local machine:

bash
Kopiera kod
git clone https://github.com/your-username/titanic-data-processing.git
Navigate to the project directory:

bash
Kopiera kod
cd titanic-data-processing
Place the train.csv file in the appropriate directory.

Usage
You can run the data processing manually or allow it to execute automatically as per the schedule.

Manual Execution
To manually run the main script and process the Titanic data:

bash
Kopiera kod
python main.py
This will:

Read the train.csv file.
Process the data (convert datatypes, handle missing values, etc.).
Save the result into an SQLite database.
Scheduled Execution
The script is configured to automatically run daily at a specific time (e.g., 12:00 PM). To run the scheduled task, ensure that main.py is running in the background:

bash
Kopiera kod
python main.py
Files
main.py: The main script that handles the workflow of reading, processing, and saving data.
read.py: Contains the function to read the CSV file.
process.py: Contains the function to process and transform the data (e.g., converting types, handling missing values).
save.py: Contains the function to save the processed data into an SQLite database.
test_main.py: Unit tests for verifying that the reading, processing, and saving functions work correctly.
Testing
To run the unit tests:

bash
Kopiera kod
python -m unittest test_main.py
The tests will check:

If the data is correctly read from the CSV file.
If the data is processed as expected (e.g., datatypes converted, missing values handled).
If the data is correctly saved to the SQLite database.
Logging
The script generates logs for all operations, which are saved to a titanic_data.log file. It records:

Successful reading and processing of data.
Successful data saving to the SQLite database.
Any exceptions or errors that occur during the process.
Future Improvements
API Integration: The project could be extended to pull data from an API instead of relying on local CSV files.
Advanced Data Processing: Additional processing steps such as feature engineering could be added.
Visualization: Data visualization scripts could be added to analyze the Titanic data directly from the database.
More Advanced Scheduling: Integration with a task scheduler like cron or Windows Task Scheduler for more flexible automation.
