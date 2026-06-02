# Office Ally Patient Automation

## Project Overview

This project was created to automate the patient registration workflow in Office Ally CMS using Playwright.

The objective was to reduce manual data entry by automating navigation to the Add New Patient page and preparing a workflow that can populate patient information from a CSV file.

The project was developed by recording user actions with Playwright Codegen, identifying selectors for required patient fields, and preparing a data-driven automation approach.

---

## Project Goals

- Automate patient creation workflow
- Reduce manual data entry
- Learn Playwright automation
- Understand selector identification
- Implement CSV-based data handling
- Explore real-world web automation

---

## Technologies Used

- Playwright
- Node.js
- VS Code
- CSV Files
- Office Ally CMS

---

## Environment Setup

### Step 1: Install Node.js

Verify installation:

bash node -v npm -v 

---

### Step 2: Create Project

bash mkdir Office-Ally-Patient-Automation cd Office-Ally-Patient-Automation 

---

### Step 3: Initialize Node Project

bash npm init -y 

This generates:

text package.json 

---

### Step 4: Install Playwright

bash npm install -D @playwright/test 

Install browsers:

bash npx playwright install 

In some environments the following command was used:

bash npx.cmd playwright install 

---

## Creating the First Test

A basic Playwright test was created to verify that the installation was successful.

Example:

javascript const { test } = require('@playwright/test');  test('Google Test', async ({ page }) => {   await page.goto('https://google.com'); }); 

Run:

bash npx.cmd playwright test --headed 

---

## Recording Office Ally Actions

Playwright Codegen was used to record browser actions automatically.

Command:

bash npx.cmd playwright codegen 

This opened:

- Browser window
- Playwright Inspector

Actions performed:

1. Open Office Ally CMS
2. Login
3. Navigate to Manage Patients
4. Open Add New Patient

Playwright automatically generated locator code.

Example:

javascript await page.getByText('Manage Patients').click();  await page.getByText('Add New Patient').click(); 

---

## Selector Identification

The following selectors were identified from the Add Patient form:

### Patient Information

- Patient Account Number
- First Name
- Last Name
- DOB
- Gender

### Address Information

- Address
- City
- State
- ZIP Code

### Contact Information

- Home Phone
- Email

### Insurance Information

- Insurance ID
- Insurance Details

These selectors were recorded using Playwright Inspector.

---

## CSV Data Preparation

A CSV file was created to store patient information.

Example:

csv PatientName,PatientAccountNumber,PatientAddress,PatientCity,PatientState,PatientZip,PatientHomePhone,Email,Sex  "Smith, John",10001,"123 Main St",Dallas,PA,75001,2145551234,john@test.com,M 

Purpose:

- Store patient data externally
- Enable data-driven testing
- Support future bulk patient creation

---

## Automation Workflow

The planned automation flow:

1. Open Office Ally CMS
2. Login
3. Navigate to Manage Patients
4. Click Add New Patient
5. Read patient data from CSV
6. Populate patient fields
7. Save patient record
8. Process next patient record

---

## Commands Used During Development

### Verify Node Installation

bash node -v npm -v 

### Initialize Project

bash npm init -y 

### Install Playwright

bash npm install -D @playwright/test 

### Install Browsers

bash npx.cmd playwright install 

### Open Code Generator

bash npx.cmd playwright codegen 

### Run Tests

bash npx.cmd playwright test --headed 

---

## Learning Outcomes

During this project, the following concepts were learned:

- Playwright Automation
- Browser Automation
- Playwright Codegen
- Selector Identification
- CSV Data Handling
- Data-Driven Testing
- Test Automation Fundamentals
- Web Application Automation

---

## Future Improvements

- Complete CSV integration
- Bulk patient creation
- Error handling
- Execution reports
- Screenshot capture
- Validation checks
- End-to-end patient onboarding automation

---

## Author

Sanvi Chawla

B.Tech Computer Science Engineering (Cyber Security)
