
# Cucumber TestNG Automation Framework

## Overview
This is a Hybrid Automation Framework built using Selenium, Cucumber, and TestNG.  
The framework supports parallel cross-browser execution, Jenkins integration, and Extent HTML reporting.
https://github.com/praveenap13/CucumberTestNGBrowser.git
---

##  Tech Stack

- Java
- Selenium 4
- Cucumber
- TestNG
- Maven
- Extent Reports
- Jenkins (CI/CD)
- ngrok

---

## Framework Features

Parallel Cross Browser Execution  
ThreadLocal WebDriver (Parallel Safe)  
Maven Command Line Support  
Jenkins Parameterized Pipeline  
Extent HTML Reporting  
Screenshot Capture on Failure  
Configurable Browser & Environment

---


## Project Structure
src/main/java
│
├── driver →  DriverFactory -> DriverManager
├── pages → Page Object classes
├──utility → ConfigReader /ElementActions/LoggerUtil/waitUtility/RetryListener

src/test/java
│
├── runners → TestNG Runner
├── context ->PageManager/TestContext
├── stepdefinitions → Step Definition files/Hooks
├── resources->features/config/extent/allure properties /testng,spark-config,log4j2 xml
└
Run specific browser:

---

##  Execution Instructions

###  Run from IDE
Right-click on `TestRunner.java` → Run as TestNG Test

---

### Run from Maven
mvn clean test -DsuiteXmlFile=src/test/resources/testng.xml -Dbrowser=edge

###  Run Cross Browser (TestNG XML)


##  Jenkins Execution

The pipeline supports parameterized browser execution.

### Available Parameters:
- chrome
- edge

Pipeline passes parameter as:

-Dbrowser=${BROWSER}
# Reports
Extent HTML report is generated at:
extent-reports/ExtentReport.html
Allure Report-target/allure-results
In Jenkins:
- Report is published automatically


---

##  Browser Resolution Priority

The framework resolves browser in the following order:

Jenkins Parameter  
Maven `-Dbrowser`  
️testng.xml parameter  
️ config.properties  
Default = chrome

---

##  Screenshot Handling

- Screenshots are captured automatically on test failure.
- Attached inside Extent report.

---

##  Parallel Execution Strategy

- Uses ThreadLocal WebDriver
- Supports parallel="tests" in TestNG
- Each thread maintains its own WebDriver instance

---

## CI/CD Ready

Jenkins Declarative Pipeline  
Email Notification with Extent Report  
HTML Report Publishing  
Parameterized Execution

---
Selenium Grid Integration
Headless Mode Support
##  Author

Praveena

---

## Future Enhancements

- Docker Execution
- Slack Notification Integration
- Environment Switching (QA/UAT/PROD)

---
