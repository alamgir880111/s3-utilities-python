Python Log Analyzer Using OOP

A Python-based log analysis tool that uses Object-Oriented Programming (OOP) to read log files, count log levels, and export the results to a JSON file.

Features

Object-Oriented Design: Uses a reusable LogAnalyzer class.

Log File Reading: Reads log entries from app2.log.

Log Level Analysis: Counts INFO, WARNING, and ERROR entries.

JSON Export: Saves the analysis results to output1.json.

Reusable Configuration: Accepts input and output filenames through the class constructor.

Technology Stack

Python 3

JSON module

File handling

Object-Oriented Programming (OOP)

Project Structure

python-log-analyzer/
├── app2.log
├── log_analyzer_class.py
├── output1.json
└── README.md

Prerequisites

Python 3 installed on your system.

An input log file named app2.log.

No third-party Python packages are required.

Getting Started

1. Clone the Repository

git clone YOUR_GITHUB_REPOSITORY_URL

Replace YOUR_GITHUB_REPOSITORY_URL with your actual GitHub repository URL.

2. Navigate to the Project Directory

cd python-log-analyzer

3. Prepare the Input Log File

Create a file named app2.log and add some sample log entries:

2026-10-19 09:00:00 INFO Application started
2026-10-19 09:01:00 WARNING High memory usage
2026-10-19 09:02:00 ERROR Database connection failed
2026-10-19 09:03:00 INFO Application running
2026-10-19 09:04:00 ERROR Request failed

4. Run the Application

Execute the following command from the project directory:

python log_analyzer_class.py

The application reads app2.log, analyzes the log entries, and writes the results to output1.json.

Example Output

The generated output1.json file will contain:

{
  "INFO": 2,
  "WARNING": 1,
  "ERROR": 2
}
