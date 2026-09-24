# Parabank Automation

Selenium-based test automation framework for the Parabank web application, built with Java, TestNG, and Maven. Supports data-driven testing using Excel input files.

## Tech Stack

- **Language:** Java
- **Test Framework:** TestNG
- **Build Tool:** Maven
- **Browser Automation:** Selenium WebDriver
- **Data-Driven Testing:** Apache POI (Excel)
- **IDE:** Eclipse

## Project Structure

```
parabank-automation/
├── src/
│   ├── main/java/          # Page objects, utilities, base classes
│   └── test/
│       ├── java/            # Test classes (TestNG)
│       │   └── dataDrivenTesting/
│       │       └── DDT_From_Excel_File.java
│       └── resources/       # Test data files (e.g., TestScriptData.xlsx)
├── test-output/             # TestNG execution reports
├── target/                  # Compiled build output (ignored in Git)
├── pom.xml                  # Maven dependencies and build config
└── testng.xml               # TestNG suite configuration
```

## Prerequisites

- Java JDK (8 or higher)
- Maven
- Eclipse IDE (with TestNG and EGit plugins)
- Chrome/Firefox browser + matching WebDriver

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/<your-username>/parabank-automation.git
   ```
2. Import into Eclipse as a Maven project (`File > Import > Existing Maven Projects`).
3. Let Maven download dependencies (`Maven > Update Project`).
4. Update any config values (base URL, credentials, file paths) as needed.

## Running Tests

- Right-click `testng.xml` → **Run As > TestNG Suite**, or
- Run via Maven:
  ```
  mvn test
  ```

Test data is read from Excel files located in `src/test/resources/`. Reports are generated in the `test-output/` folder after each run.

## Notes

- Excel test data is read using Apache POI in `DDT_From_Excel_File.java`.
- Add new test scenarios by adding rows to the Excel data file, no code changes required for new data sets.

## Author

Jothirupan
