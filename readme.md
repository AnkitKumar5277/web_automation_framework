# 🚀 Web Automation Framework (Python + Selenium + PyTest)

A robust **Web Automation Framework** built with **Python, Selenium, and PyTest** using **Page Object Model (POM)** and **Page Factory** design patterns.  
Supports **parallel execution, reporting, database validation, and environment management**.  
---

## 🛠 Tech Stack
- **Language**: Python  
- **Test Runner**: PyTest  
- **Automation Tool**: Selenium  
- **Design Pattern**: Page Object Model (POM) + Page Factory  
- **Reports**: Allure Report, PyTest HTML Report  
- **Parallel Execution**: PyTest-xdist  
- **Database**: MySQL (for data validation)  
- **Others**: Faker (test data generation), dotenv (environment management)  

---

## 📂 Framework Features
- ✅ Page Object Model (POM) & Page Factory  
- ✅ Highlight element during execution  
- ✅ Allure & PyTest HTML Reports  
- ✅ Parallel test execution with `pytest-xdist`  
- ✅ MySQL database connection for data validation  
- ✅ Environment variables via `.env`  
- ✅ ReportPortal integration  
- ✅ Modular and scalable folder structure  

---

## 📦 Installation

Clone the repo and install dependencies:  

git clone https://github.com/your-username/web-automation-framework.git
cd web-automation-framework

Install required dependencies:

pip install allure-pytest selenium
pip install pytest selenium pytest-html openpyxl
pip install selenium-page-factory
pip install pyyaml faker openpyxl
pip install pytest-xdist
pip install mysql-connector-python
pip install pytest-reportportal
pip install python-dotenv

▶️ How to Run the Tests?

Run all test cases:

pytest -n auto tests/vwoLoginTests/pom/test_*


Run a specific test case in parallel:

pytest -n auto tests/test/vwoLoginTests/test_vwo_login.py

📊 Reports
Allure Report

Generate and open Allure report:

pytest --alluredir=reports/allure-results
allure serve reports/allure-results

PyTest HTML Report

Generate PyTest HTML report:

pytest --html=reports/report.html --self-contained-html

⚙️ Project Structure
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

🗄 Database Validation (MySQL)

The framework connects to MySQL database to validate test data.

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

🌐 Environment Management

Sensitive credentials & environment-specific details are stored in .env file.

Example .env file:

BASE_URL=https://app.vwo.com
USERNAME=your-username
PASSWORD=your-password
DB_HOST=localhost
DB_USER=root
DB_PASS=password


Load them in code:

from dotenv import load_dotenv
import os

load_dotenv()
username = os.getenv("USERNAME")
password = os.getenv("PASSWORD")

🏃 Parallel Execution

Leverage pytest-xdist for parallel execution:

pytest -n auto

📢 Contributions

Contributions are welcome! Please fork the repo and raise a PR. 🚀

📜 License

This project is licensed under the MIT License.


---






