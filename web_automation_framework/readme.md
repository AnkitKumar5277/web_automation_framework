🧪 Web Automation Framework (Python + Selenium + POM)

This repository contains a Web Automation Testing Framework built with Python, Selenium, and PyTest.
It follows the Page Object Model (POM) and Page Factory design pattern for scalability and maintainability.

🚀 Tech Stack
Language: Python
Test Runner: PyTest
Automation Tool: Selenium
Reporting: Allure Reports, PyTest HTML Reports
Parallel Execution: PyTest-xdist
Database Validation: MySQL Connector
Data Management: OpenPyXL, Faker, YAML, dotenv

📂 Features
✔ Page Object Model (POM) and Page Factory
✔ Highlight elements while execution
✔ Parallel test execution with pytest-xdist
✔ Allure & HTML reports integration
✔ MySQL DB connectivity for validation
✔ External test data handling with Excel, YAML, .env
✔ ReportPortal integration (optional)

⚙️ Installation
Clone the repository and install dependencies:
pip install allure-pytest selenium
pip install pytest selenium pytest-html openpyxl
pip install selenium-page-factory
pip install pyyaml faker openpyxl
pip install pytest-xdist
pip install mysql-connector-python
pip install pytest-reportportal
pip install python-dotenv

▶️ How to Run the Tests?
Run all test cases (parallel execution)
pytest -n auto tests/vwoLoginTests/pom/test_*

Run a specific test case
pytest -n auto tests/vwoLoginTests/test_vwo_login.py

📊 Reports
Generate Allure Report
pytest --alluredir=reports/allure-results
allure serve reports/allure-results

Generate PyTest HTML Report
pytest --html=reports/report.html --self-contained-html

🗄 MySQL Database Validation
This framework connects to MySQL database to verify test data.
You can configure DB credentials in .env file:

DB_HOST=localhost
DB_USER=root
DB_PASS=password
DB_NAME=test_db

🔧 Gitignore
__pycache__/
*.pyc
.env
reports/
allure-results/
allure-report/