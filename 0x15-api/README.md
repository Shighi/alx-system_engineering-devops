# API Data Retrieval Project

## Description
This project focuses on retrieving and processing employee TODO list data from a REST API. It includes functionality to export the data in various formats (CSV, JSON) and provides progress tracking for employee tasks.

## Project Requirements

### General
- All files must be interpreted/compiled on Ubuntu 20.04 LTS using Python 3.8.5
- All files must end with a newline character
- The first line of all files must be exactly `#!/usr/bin/python3`
- Libraries must be imported in alphabetical order
- Code must adhere to pycodestyle (version 2.8.*)
- All files must be executable
- All modules must be documented: `python3 -c 'print(__import__("my_module").__doc__)'`
- Dictionary values must be accessed using `get` method
- Code should not be executed when imported

### Execution Environment
- **Allowed editors**: vi, vim, emacs
- **Python version**: 3.8.5
- **OS**: Ubuntu 20.04 LTS

## Tasks

### 0. Gather data from an API
**File**: `0-gather_data_from_an_API.py`

Writes a Python script that retrieves TODO list progress for a given employee ID using a REST API. The script:
- Uses `urllib` or `requests` module
- Accepts an integer as parameter (employee ID)
- Displays employee TODO list progress in the format:
  ```
  Employee EMPLOYEE_NAME is done with tasks(NUMBER_OF_DONE_TASKS/TOTAL_NUMBER_OF_TASKS):
      TASK_TITLE
      TASK_TITLE
      ...
  ```

### 1. Export to CSV
**File**: `1-export_to_CSV.py`

Extends the previous script to export data in CSV format:
- Records all tasks owned by the employee
- Format: `"USER_ID","USERNAME","TASK_COMPLETED_STATUS","TASK_TITLE"`
- File name: `USER_ID.csv`

### 2. Export to JSON
**File**: `2-export_to_JSON.py`

Extends the script to export data in JSON format:
- Records all tasks owned by the employee
- Format:
  ```json
  {
    "USER_ID": [
      {
        "task": "TASK_TITLE",
        "completed": TASK_COMPLETED_STATUS,
        "username": "USERNAME"
      },
      ...
    ]
  }
  ```
- File name: `USER_ID.json`

### 3. Dictionary of list of dictionaries
**File**: `3-dictionary_of_list_of_dictionaries.py`

Further extends the script to export all tasks from all employees in JSON format:
- Records all tasks from all employees
- Format:
  ```json
  {
    "USER_ID": [
      {
        "username": "USERNAME",
        "task": "TASK_TITLE",
        "completed": TASK_COMPLETED_STATUS
      },
      ...
    ],
    "USER_ID": [
      ...
    ]
  }
  ```
- File name: `todo_all_employees.json`

## Repository Information
- **GitHub repository**: `alx-system_engineering-devops`
- **Directory**: `0x15-api`
