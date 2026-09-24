<div align="center">

# 🏦 Parabank Automation

**A robust, data-driven Selenium test automation framework for the Parabank web application**

[![Java](https://img.shields.io/badge/Java-8%2B-orange?style=flat-square&logo=openjdk)](https://www.oracle.com/java/)
[![Selenium](https://img.shields.io/badge/Selenium-WebDriver-43B02A?style=flat-square&logo=selenium)](https://www.selenium.dev/)
[![TestNG](https://img.shields.io/badge/TestNG-Framework-orange?style=flat-square)](https://testng.org/)
[![Maven](https://img.shields.io/badge/Build-Maven-C71A36?style=flat-square&logo=apachemaven)](https://maven.apache.org/)
[![Apache POI](https://img.shields.io/badge/Data--Driven-Apache%20POI-blue?style=flat-square)](https://poi.apache.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](#license)

[Overview](#-overview) •
[Tech Stack](#-tech-stack) •
[Project Structure](#-project-structure) •
[Getting Started](#-getting-started) •
[Running Tests](#-running-tests) •
[Reports](#-test-reports) •
[Contributing](#-contributing)

</div>

---

## 📖 Overview

**Parabank Automation** is a Selenium WebDriver-based UI test automation framework built for the [Parabank](https://parabank.parasoft.com/) demo banking application. It follows the **Page Object Model (POM)** design pattern and uses **data-driven testing** so QA engineers can add new test scenarios by editing an Excel file — no code changes required.

### ✨ Key Features

- 🧩 **Page Object Model** architecture for clean separation of test logic and UI locators
- 📊 **Data-Driven Testing** via Apache POI — drive scenarios directly from Excel (`.xlsx`)
- ⚙️ **TestNG** suite management with configurable, parallel-ready execution
- 📁 Centralized, reusable base classes and utility methods
- 📝 Auto-generated **TestNG HTML/XML reports** after every run
- 🔧 **Maven**-managed dependencies and build lifecycle
- 🌐 Cross-browser support (Chrome / Firefox)

---

## 🛠 Tech Stack

| Category | Technology |
|---|---|
| **Language** | Java 8+ |
| **Test Framework** | TestNG |
| **Build Tool** | Maven |
| **Browser Automation** | Selenium WebDriver |
| **Data-Driven Testing** | Apache POI (Excel) |
| **IDE** | Eclipse |

---

## 📂 Project Structure

```
parabank-automation/
├── src/
│   ├── main/java/                        # Page objects, utilities, base classes
│   └── test/
│       ├── java/                         # TestNG test classes
│       │   └── dataDrivenTesting/
│       │       └── DDT_From_Excel_File.java
│       └── resources/                    # Test data files (e.g., TestScriptData.xlsx)
├── test-output/                          # TestNG execution reports (generated)
├── target/                               # Compiled build output (git-ignored)
├── pom.xml                               # Maven dependencies & build config
└── testng.xml                            # TestNG suite configuration
```

---

## ✅ Prerequisites

Make sure the following are installed before setup:

- [Java JDK 8+](https://www.oracle.com/java/technologies/downloads/)
- [Maven](https://maven.apache.org/download.cgi)
- [Eclipse IDE](https://www.eclipse.org/downloads/) with **TestNG** and **EGit** plugins
- Chrome/Firefox browser with a matching WebDriver version

---

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/parabank-automation.git
   cd parabank-automation
   ```

2. **Import into Eclipse**
   `File > Import > Existing Maven Projects` → select the cloned folder

3. **Resolve dependencies**
   Right-click the project → `Maven > Update Project`

4. **Configure environment**
   Update base URL, credentials, and file paths in the relevant config/properties file as needed

---

## ▶️ Running Tests

**Option 1 — Via Eclipse**
Right-click `testng.xml` → **Run As → TestNG Suite**

**Option 2 — Via Maven CLI**
```bash
mvn test
```

> 💡 Test data is read from Excel files in `src/test/resources/`. To add a new scenario, simply add a row to the Excel file — no code changes required.

---

## 📊 Test Reports

After execution, TestNG automatically generates reports in the `test-output/` directory:

- `test-output/index.html` — interactive summary report
- `test-output/emailable-report.html` — shareable summary report

---

## 🗂 Data-Driven Testing

Test scenarios are driven from `TestScriptData.xlsx` and parsed using **Apache POI** inside [`DDT_From_Excel_File.java`](src/test/java/dataDrivenTesting/DDT_From_Excel_File.java).

To add a new test case:
1. Open the Excel data file in `src/test/resources/`
2. Add a new row with the required test parameters
3. Run the suite — no code changes needed

---

## 🗺 Roadmap

- [ ] Integrate CI/CD pipeline (GitHub Actions / Jenkins)
- [ ] Add cross-browser parallel execution
- [ ] Extend reporting with Extent/Allure reports
- [ ] Add Dockerized execution environment

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**Jothirupan**

<div align="center">

⭐ If you find this project useful, consider giving it a star!

</div>
