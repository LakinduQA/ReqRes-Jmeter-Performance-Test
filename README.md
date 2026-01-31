# ReqRes.com JMeter Test Suite

This project is a **performance and functional API test suite** for [https://reqres.in/](https://reqres.in/), built using **Apache JMeter**. It simulates realistic user scenarios such as registration, login, data retrieval, creation, update, and deletion, while generating detailed performance reports.

<p align="left">
  <img src="https://img.shields.io/badge/Apache%20JMeter-5.6+-D22128?logo=apache&logoColor=white" alt="Apache JMeter">
  <img src="https://img.shields.io/badge/Java-17+-007396?logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/API-ReqRes-FF6C37?logo=postman&logoColor=white" alt="ReqRes API">
  <img src="https://img.shields.io/badge/Test%20Type-Performance-brightgreen" alt="Performance Testing">
  <img src="https://img.shields.io/badge/Reports-HTML-E34F26?logo=html5&logoColor=white" alt="HTML Reports">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
</p>


## Features

- **Well-Structured Test Plan**: Each API endpoint is neatly organized for better readability and maintenance.
- **Data-Driven Testing**: Uses CSV files for testing dynamic input like user creation and update.
- **Assertions**: Verifies both status codes and response content.
- **Simulated User Behavior**: Timers introduce delays to mimic real-world user interaction.
- **Comprehensive Reporting**: Includes tree, table, summary, aggregate, and assertion reports.
- **Centralized Config**: Global variables and request defaults are separated for easy editing.

---

## JMeter Test Components

```
ReqRes API Test Plan
├── HTTP Configuration:
│   ├── User Defined Variables
│   ├── HTTP Header Manager
│   └── HTTP Request Defaults
├── CSV Data Set Config:
│   ├── createUser.csv
│   └── updateUser.csv
├── Thread Group - reqres
│   ├── userRegistration
│   ├── userLogin
│   ├── getUserList
│   ├── getSingleUser
│   ├── createNewUser
│   ├── updateUserData
│   └── deleteUser
├── Timers:
│   ├── Constant Timer
│   └── Uniform Random Timer
├── JSON Extractors
├── Assertions
└── Listeners:
    ├── View Results Tree
    ├── View Results in Table
    ├── Summary Report
    ├── Aggregate Report
    └── Assertion Results
```

---

## Project Folder Layout

```
ReqResAPI-Performance Test/
├── csv files - ddt/             # CSV test data files for create/update operations
├── HTML Report/                 # Auto-generated visual performance report
├── results/                     # Contains output from all JMeter listeners
├── Screenshots/                # Manual screenshots taken of test execution and results
└── ReqResAPI_PerformanceTest.jmx  # The main JMeter test plan file
```

---

## How to Run

1. **Install JMeter**  
   Download from: [https://jmeter.apache.org/download_jmeter.cgi](https://jmeter.apache.org/download_jmeter.cgi)

2. **Open Project**  
   Open `ReqResAPI_PerformanceTest.jmx` in JMeter.

3. **Set Up Data**  
   Ensure your CSV files are in the `csv files - ddt/` folder.

4. **Run the Test Plan**  
   Click the **Start** button in JMeter.

5. **View Reports**
   - Open `HTML Report/` for a detailed graphical report.
   - Check `results/` for raw listener outputs.
   - See `Screenshots/` for manually captured test results.

---

## Notes
- Excessive or rapid API requests might trigger temporary blocks because of rate limits
