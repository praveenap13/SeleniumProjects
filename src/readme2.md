
# Rest Assured Automation Framework

## Overview
This is a Rest Assured Automation Framework built using Selenium and TestNG.  
Jenkins integration, and Extent HTML reporting.
https://github.com/praveenap13/RestAssuredLion.git
---

##  Tech Stack

- Java
- Selenium 4
- TestNG
- Maven
- Extent Reports
- Allure Report
- Jenkins (CI/CD)

---

## Framework Features

Maven Command Line Support
Extent HTML Reporting  
Screenshot Capture on Failure  
Configurable Browser & Environment

---


## Project Structure
src/main/java
│
├── helpers
├── requestModels
├──utils → BaseService /CommonFunctionAndAPIVarification/RestAssuredListener/TestListener

src/test/java
│
├── listener → TestNG Runner
├── tests ->PageManager/TestContext
├── resources->requestPayload/config,log4j2 properties
└
pom.xml
testng.xml

---

##  Execution Instructions

###  Run from IDE
Right-click on `TestRunner.java` → Run as TestNG Test

---

### Run from Maven
mvn clean test -Dsuitefilename=testng.xml



##  Jenkins Execution

Pipeline Created


# Reports
Extent HTML report is generated at:
extent-reports/ExtentReport.html
Allure Report-target/allure-results
In Jenkins:
Report is published automatically

---


## CI/CD Ready

Jenkins Declarative Pipeline
Report Publishing  

##  Author

Praveena


