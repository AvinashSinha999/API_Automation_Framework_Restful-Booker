# 🚀 API Automation Framework | Restful Booker

> A modular **API Automation Framework** built using **Java**, **Rest-Assured**, **TestNG**, **Maven**, **GSON**, **AssertJ**, and **Allure Reports** to automate testing of the **Restful Booker** APIs.

<p align="center">

![Java](https://img.shields.io/badge/Java-11+-blue?logo=openjdk)
![Maven](https://img.shields.io/badge/Maven-Build%20Tool-C71A36?logo=apachemaven&logoColor=white)
![RestAssured](https://img.shields.io/badge/RestAssured-API--Testing-yellowgreen)
![TestNG](https://img.shields.io/badge/TestNG-Framework-brightgreen)
![AssertJ](https://img.shields.io/badge/AssertJ-Assertions-orange)
![GSON](https://img.shields.io/badge/GSON-POJO%20Serialization-lightgrey)
![Allure](https://img.shields.io/badge/Allure-Reports-ff69b4)
![Log4j2](https://img.shields.io/badge/Log4j2-Logging-yellow)

</p>

---

# 🗂️ Overview

This repository contains a modular **API Automation Framework** for testing the **Restful Booker** APIs.

Built with **Java**, **Rest-Assured**, **TestNG**, and **Maven**, the framework demonstrates industry-standard API automation practices including **POJO-based payload serialization**, **authentication**, **CRUD operations**, reusable assertion utilities, end-to-end workflow testing, logging, and interactive Allure reporting.

The framework uses **GSON** for request and response serialization/deserialization, providing clean, type-safe, and maintainable API test automation.

---

# ✨ Features

- ✅ Complete CRUD API Automation
- ✅ Token-Based Authentication
- ✅ POJO-Based Payload Serialization
- ✅ Modular Framework Design
- ✅ Centralized Assertion Utilities
- ✅ End-to-End Integration Testing
- ✅ TestNG Suite Execution
- ✅ Log4j2 Logging
- ✅ Allure Reporting

---

# 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| Java 11+ | Programming Language |
| Maven | Dependency & Build Management |
| Rest-Assured | API Automation |
| TestNG | Test Framework |
| AssertJ | Fluent Assertions |
| GSON | POJO Serialization & Deserialization |
| Log4j2 | Logging |
| Allure Reports | Test Reporting |
| IntelliJ IDEA | Development IDE |

---

# 🏗️ Project Structure

```text
API_Automation_Framework_RestfulBooker/
│
├── .idea/                                                    # IntelliJ config
├── .mvn/                                                     # Maven wrapper files
├── allure-results/                                           # Allure results (auto-generated)
│
├── pom.xml                                                   # Project dependencies & build config
├── .gitignore
├── testng_*.xml                                              # TestNG suite files
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com.avinashsinha.endpoints/
│   │   │   │   └── APIConstants.java                         # API endpoint constants
│   │   │   │
│   │   │   ├── com.avinashsinha.modules/
│   │   │   │   └── PayloadManager.java                       # Payload manager
│   │   │   │
│   │   │   └── com.avinashsinha.pojos/
│   │   │       ├── Auth.java
│   │   │       ├── Booking.java
│   │   │       ├── BookingDates.java
│   │   │       ├── BookingResponse.java
│   │   │       └── TokenResponse.java
│   │   │
│   │   └── resources/
│   │       └── log4j2.xml                                    # Logging configuration
│   │
│   └── test/
│       └── java/
│           ├── com.avinashsinha.asserts/
│           │   └── AssertActions.java                        # Assertion utilities
│           │
│           ├── com.avinashsinha.base/
│           │   └── BaseTest.java                             # Base test configuration
│           │
│           └── com.avinashsinha.tests/
│               ├── crud/                                     # CRUD Test Cases
│               │   ├── TestBookingCreate.java
│               │   ├── TestBookingDateValidation.java
│               │   ├── TestBookingDeletion.java
│               │   ├── TestBookingFullUpdate.java
│               │   ├── TestBookingPartialUpdate.java
│               │   ├── TestBookingVerificationById.java
│               │   ├── TestBookingVerificationByName.java
│               │   ├── TestCheckHealth.java
│               │   └── TestTokenCreate.java
│               │
│               ├── integration/                              # Integration Test Cases
│               │   └── TestE2EFlow.java
│               │
│               └── sample/                                   # Sample Tests
│                   └── TestIntegrationSample.java
│
└── README.md
```

---

# 📦 Framework Components

| Component | Description |
|------------|-------------|
| **APIConstants** | Stores all API endpoint constants |
| **PayloadManager** | Creates reusable POJO request payloads |
| **POJOs** | Request and response serialization models |
| **BaseTest** | Provides common test setup and configuration |
| **AssertActions** | Centralized assertion utilities |
| **CRUD Tests** | Individual booking API test scenarios |
| **Integration Tests** | End-to-end booking workflow validation |
| **Resources** | Log4j2 configuration files |

---

# ✅ Test Coverage

| Endpoint | Test Scenario |
|-----------|---------------|
| **POST** `/auth` | Generate Authentication Token |
| **GET** `/ping` | Health Check |
| **POST** `/booking` | Create Booking |
| **GET** `/booking/{id}` | Retrieve Booking by ID |
| **GET** `/booking` | Verify Booking by Name |
| **GET** `/booking` | Verify Booking by Date |
| **PUT** `/booking/{id}` | Full Update Booking |
| **PATCH** `/booking/{id}` | Partial Update Booking |
| **DELETE** `/booking/{id}` | Delete Booking |
| Workflow | End-to-End Integration Testing |

---

# ▶️ Running Tests

Execute any TestNG suite using Maven.

### Example

```bash
mvn clean test -DsuiteXmlFile=testng_Integration.xml
```

### Available Test Suites

| Suite | XML File |
|--------|----------|
| Create Booking | `testng_createBooking.xml` |
| Delete Booking | `testng_deleteBookingId.xml` |
| Full Update | `testng_fullUpdate.xml` |
| Partial Update | `testng_partialUpdate.xml` |
| Verify by ID | `testng_verifyByID.xml` |
| Verify by Name | `testng_verifyByName.xml` |
| Verify by Date | `testng_verifyByDate.xml` |
| Sample Tests | `testng_sample.xml` |
| End-to-End Flow | `testng_Integration.xml` |

---

# 📊 Allure Reports

Generate the report using:

```bash
allure serve allure-results
```

<p align="center">
<img width="1100" src="https://github.com/user-attachments/assets/4e746c4a-78d6-4c0d-9e67-492ff048c799" alt="Restful Booker Allure Report">
</p>

The command launches an interactive Allure dashboard in your default browser.

---

# 📝 Sample POJO-Based Payload

```java
Booking booking = new Booking();

booking.setFirstname("John");
booking.setLastname("Doe");
booking.setTotalprice(120);
booking.setDepositpaid(true);

BookingDates bookingDates = new BookingDates();
bookingDates.setCheckin("2025-10-01");
bookingDates.setCheckout("2025-10-05");

booking.setBookingdates(bookingDates);
booking.setAdditionalneeds("Lunch");
```

---

# 👨‍💻 Author

**Avinash Sinha**

If you found this repository helpful, consider giving it a ⭐ on GitHub.

---

# 📄 License

This project is intended for **educational** and **learning purposes**.
