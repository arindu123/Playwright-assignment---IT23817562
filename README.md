# Automated Testing of SwiftTranslator Web Application

**ITPM Assignment 1 – Automated Web Testing using Playwright**

This project presents an automated testing solution developed for the SwiftTranslator web application (https://swifttranslator.com
), which converts Singlish text into Sinhala.
The objective of this assignment is to apply automated testing concepts and tools learned in the IT3040 – IT Project Management (ITPM) module.

## Project Overview

The objective of this project is to automate the testing process of the SwiftTranslator system using Playwright. Instead of manually verifying translations, the test suite executes multiple predefined scenarios automatically, 
ensuring the reliability and correctness of the system.
The automation validates:
  Translation accuracy for common Singlish sentences
  System behavior for various sentence structures
  Handling of invalid or unusual inputs (typos, spacing issues, symbols)
  User interface responses such as real-time translation updates
  
## Test Scope

**Functional Testing (34 Test Cases)**
Positive Functional Tests (24)
Validate correct translations for valid Singlish inputs

Negative Functional Tests (10)
Evaluate robustness using incorrect formats, spacing issues, and noisy inputs

**UI Testing (1 Test Case)**
-Verifies that the input field accepts typing correctly

## Project Structure

```
Playwright-assignment---IT23817562/
├── tests/
│   └── translator.spec.js       # Automated test script
├── test-data/
│   └── cases.js                 # Defined test cases
├── playwright.config.js         # Playwright configuration file
├── package.json                 # Project dependencies
└── README.md                    # Project documentation
                  # This file
```

## Setup Instructions

### Prerequisites

You need Node.js installed on your computer. Download it from https://nodejs.org (get the LTS version).

Check if it's installed:
```bash
node -v
npm -v
```

### Installation

1. Clone this repository
```bash
git clone https://github.com/arindu123/Playwright-assignment---IT23817562.git
cd Playwright-assignment---IT23817562
```

2. Install dependencies
```bash
npm install
```

3. Install Playwright browsers
```bash
npx playwright install
```

## Running the Tests

Run all tests:
```bash
npx playwright test 
```

Run a specific test:
```bash
npx playwright test -g "Pos_Fun_0004"
```

Run without opening browser window:
```bash
npx playwright test --project=chromium
```

## Viewing Results

After tests finish, view the HTML report:
```bash
npx playwright show-report
```

The report shows which tests passed or failed, how long they took, and any error messages.

## Test Design Approach

Test cases are defined separately in test-data/cases.js
Each test case includes:
  Test case ID
  Input data
  Expected behavior or output
  Test description

The main test script iterates through these cases and performs automated validation using assertions.

## Notes

- Need an internet connection to run these tests
- Tests use Chromium browser for consistency
- Don't close the browser manually while tests are running
- Some outputs might vary slightly due to how the translation system works

## Technologies Used

- **Playwright** - Browser automation framework
- **Node.js** - JavaScript runtime
- **Chromium** - Testing browser
- **JavaScript** - Programming language

## Author

**Student Name:** Arindu Semal

**Registration Number:** IT23817562

**Module Code: IT3040 –** IT Project Management

**Institution:** Sri Lanka Institute of Information Technology (SLIIT)

