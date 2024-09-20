Titanic Data Processing and SQL Storage
This project automates the process of reading, processing, and saving Titanic passenger data from the train.csv file to an SQL database. The system is built with Python and uses Pandas for data manipulation, SQLite for data storage, and unittest for automated testing.

Features
Automated Data Pipeline: The program reads Titanic data from a CSV file, processes and formats it (e.g., handling missing values, converting data types), and stores the processed data in a local SQLite database.
Data Processing: Specific columns are selected from the Titanic dataset, and new columns (e.g., IsChild) are created to categorize passengers based on age.
SQL Database Storage: The processed data is saved into an SQLite database, making it easy to query and analyze in the future.
Error Handling & Logging: All errors during execution are logged to a file, making debugging easier.
Automated Tests: The system includes unit tests to ensure that data reading, processing, and saving functionalities work as expected.
Project Structure
bash
Kopiera kod
├── kunskapskontroll_2/
│   ├── read.py              # Reads Titanic data from CSV
│   ├── process.py           # Processes and formats the Titanic data
│   ├── save.py              # Saves the processed data into an SQLite database
│   ├── main.py              # The main script to orchestrate the workflow
│   ├── test_main.py         # Automated tests for the project
│   └── train.csv            # Titanic dataset (train.csv)
└── README.md                # Project documentation
Requirements
Python 3.x
Libraries:
pandas
sqlite3 (built-in with Python)
unittest
schedule (for scheduling tasks)
You can install the necessary Python libraries using pip:

bash
Kopiera kod
pip install pandas schedule
How to Run
Set up your environment:

Clone the repository or download the project files.
Make sure you have the necessary dependencies installed (see "Requirements" above).
Prepare the dataset:

The project uses the train.csv file from the Titanic dataset. This file should be placed in the kunskapskontroll_2 folder.
Run the main script:

To execute the entire pipeline (from reading data to saving it in the SQL database), run the following command in the terminal:
bash
Kopiera kod
python main.py
This will:

Read Titanic data from train.csv.
Process the data (e.g., handling missing values and creating new columns).
Save the processed data to an SQLite database.
View the log file:

All actions are logged in a log file (titanic_data.log) located in the project directory. This log file will show if any errors occurred or if everything ran smoothly.
Run Automated Tests:

To run unit tests and verify that everything is functioning as expected, use the following command:
bash
Kopiera kod
python -m unittest test_main.py
Data Processing
During processing, the following operations are performed:

Handling Missing Values: Missing values in the Age column are filled with the median age.
Type Conversion: The Age and Fare columns are converted to float to ensure consistency.
Feature Engineering: A new column IsChild is created, classifying passengers as either Child (age < 18) or Adult.
Database
The processed data is stored in an SQLite database. The default database name is titanic_database.db, and the processed data is saved in a table called TitanicTrainData. You can view and query this database using tools like DB Browser for SQLite.

Testing
The project uses unittest to test the following components:

Data Reading: Ensures that the train.csv file is correctly read into a Pandas DataFrame.
Data Processing: Verifies that the data is processed correctly, including type conversions and the creation of the IsChild column.
Data Saving: Tests whether the processed data is correctly saved to an SQLite database and that the number of saved rows matches the input data.
To run the tests:

bash
Kopiera kod
python -m unittest test_main.py
Schedule Automated Execution
You can schedule the main script to run at regular intervals (e.g., every day at a specific time) using the schedule library. The main.py script is already configured to run the job daily at 12:00.

License
This project is open source and available under the MIT License.
