
# Cucumber TestNG Automation Framework

## Overview
This is a Hybrid Automation Framework built using Selenium, Cucumber, and TestNG.  
The framework supports parallel cross-browser execution, Jenkins integration, and Extent HTML reporting.

---

##  Tech Stack

- Java
- Selenium 4
- Cucumber
- TestNG
- Maven
- Extent Reports
- Jenkins (CI/CD)

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
src/test/java
│
├── runners → TestNG Runner
├── factory → DriverFactory (ThreadLocal)
├── hooks → Cucumber Hooks
├── stepdefinitions → Step Definition files
├── pages → Page Object classes
└── utils → Config Reader / Utilities
Run specific browser:

---

##  Execution Instructions

###  Run from IDE
Right-click on `TestRunner.java` → Run as TestNG Test

---

### Run from Maven

Run default browser (from config file):
mvn clean test

mvn clean test -Dbrowser=chrome
mvn clean test -Dbrowser=edge

###  Run Cross Browser (TestNG XML)
###  Run Cross Browser (TestNG XML)

##  Jenkins Execution

The pipeline supports parameterized browser execution.

### Available Parameters:
- chrome
- edge

Pipeline passes parameter as:

-Dbrowser=${BROWSER}
Extent HTML report is generated at:
Extent HTML report is generated at:
target/extent-reports/ExtentReport.html
In Jenkins:
- Report is published automatically
- Report is attached in email notification

---

##  Browser Resolution Priority

The framework resolves browser in the following order:

Jenkins Parameter  
Maven `-Dbrowser`  
️  testng.xml parameter  
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

##  Author

Praveena

---

## Future Enhancements

- Selenium Grid Integration
- Docker Execution
- Headless Mode Support
- Slack Notification Integration
- Environment Switching (QA/UAT/PROD)

---
