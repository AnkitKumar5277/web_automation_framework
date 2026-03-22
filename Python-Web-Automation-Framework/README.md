### Web Automation Framework (Python + Selenium + POM)
A robust Web Automation Framework built with Python, Selenium, and PyTest using Page Object Model (POM) and Page Factory design patterns.
Supports parallel execution, reporting, database validation, and environment management.

### Tech Stack
- Language: Python
- Test Runner: PyTest
- Automation Tool: Selenium
- Reporting: Allure Reports, PyTest HTML Reports
- Parallel Execution: PyTest-xdist
- Database Validation: MySQL Connector
- Data Management: OpenPyXL, Faker, YAML, dotenv

### Features
✔ Page Object Model (POM) and Page Factory  
✔ Highlight elements while execution  
✔ Parallel test execution with pytest-xdist  
✔ Allure & HTML reports integration  
✔ MySQL DB connectivity for validation  
✔ External test data handling with Excel, YAML, .env  
✔ ReportPortal integration (optional)

### Run all test cases (parallel execution)
```
pytest -n auto tests/vwoLoginTests/pom/test_*
```
### Run a specific test case
```
pytest -n auto tests/vwoLoginTests/test_vwo_login.py
```
### Generate Allure Report
```
pytest --alluredir=reports/allure-results
```
```
allure serve reports/allure-results
```
### Generate PyTest HTML Report
```
pytest --html=reports/report.html --self-contained-html
```
### MySQL Database Validation
This framework connects to MySQL database to verify test data.
You can configure DB credentials in .env file:
```
import mysql.connector

conn = mysql.connector.connect(
    host="localhost",
    user="root",
    password="password",
    database="test_db"
)
cursor = conn.cursor()
cursor.execute("SELECT * FROM users;")
result = cursor.fetchall()
print(result)
```

### Environment Management
Sensitive credentials & environment-specific details are stored in .env file.
Example .env file:
```
DB_HOST=localhost
DB_USER=root
DB_PASS=password
DB_NAME=test_db
```
Load them in code:
```
from dotenv import load_dotenv
import os

load_dotenv()
username = os.getenv("USERNAME")
password = os.getenv("PASSWORD")
```


### Project Structure
```
project-root/
│── tests/
│   ├── vwoLoginTests/
│   │   ├── pom/
│   │   │   └── test_*.py
│   ├── pageObjects/
│   ├── utils/
│   ├── constants/
│   └── __init__.py
│
│── .env
│── pytest.ini
│── requirements.txt
│── README.md
│── .gitignore
```


![Screenshot 2024-11-22 at 9 12 15 PM](https://github.com/user-attachments/assets/1108a0d3-2f71-472a-8121-f4f3d62f1291)


Dry Run Testcases 

![Screenshot 2025-01-24 at 8 52 25 PM](https://github.com/user-attachments/assets/09bdd621-9e36-4787-846b-75a8332e0666)
