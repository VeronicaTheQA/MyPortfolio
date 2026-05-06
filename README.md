# Hi, I'm Veronica! 👋

I am a Results‑driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise platforms. I specialize in TypeScript‑based Playwright test automation that integrates Faker.js for data generation, axe‑core for accessibility, and SheetJS for Excel‑based validation.

---

## 👩‍💻 Tech Stack & Badges

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)](https://playwright.dev/)
[![Faker.js](https://img.shields.io/badge/Faker.js-000000?style=for-the-badge&logo=faker&logoColor=white)](https://fakerjs.dev/)
[![SheetJS](https://img.shields.io/badge/SheetJS-000000?style=for-the-badge&logo=xlsx&logoColor=white)](https://sheetjs.com/)
[![axe-core](https://img.shields.io/badge/axe--core-000000?style=for-the-badge)](https://www.deque.com/axe/)

---

## Skills

- **Testing Types:** QA Testing, Regression, Smoke, UAT, API Testing, End‑to‑End Testing, Exploratory Testing, Mobile Testing, UI/UX Testing, Compatibility Testing, Performance Testing, Accessibility Testing, Section 508 Testing
- **Automation & Testing Tools:** Playwright, Selenium, JMeter, Postman, axe‑core, Faker.js, SheetJS, LoadRunner, BrowserStack, Charles Proxy
- **Languages & Scripting:** TypeScript, JavaScript, HTML, CSS, SQL
- **Databases:** MySQL, PostgreSQL, Cosmos DB, Data Validation & Verification
- **Platforms & DevOps:** Azure DevOps, CI/CD, Jenkins, GitHub, GitLab, SAP, Salesforce
- **Project Management:** Jira, Confluence, Zephyr, Trello, SDLC, STLC, Defect Tracking, Agile/Scrum
- **Soft Skills:** Problem‑solving, Critical Thinking, Analytical Thinking, Decision‑making, Communication, Project Management

---

## My QA & Automation Approach

- Prefer **TypeScript‑based Playwright frameworks** with Page Object Model and data‑driven tests.  
- Emphasize **API and UI test coverage** together, not just UI alone.  
- Use **Faker.js** for dynamic, realistic data and **SheetJS** for Excel‑based validation.  
- Integrate **axe‑core accessibility checks** into CI/CD pipelines for Section 508‑style testing.  
- Write clear, reusable test scripts and documentation so they double as living examples.

---

## How to Use This Repo

- Run UI tests:  
  ```bash
  npx playwright test --project chromium
  ```
- Generate new tests:  
  ```bash
  npx playwright codegen https://example.com
  ```
- Validate accessibility: run axe‑core‑integrated tests and review the HTML report.  
- Use Faker‑generated data in your own forms by importing `@faker-js/faker`.  
- Read Excel files by calling SheetJS after downloading reports from a web app (e.g., child care portals, Salesforce exports).

---

## Playwright + TypeScript Test Automation Framework

A scalable UI and API test automation framework built with **Playwright** and **TypeScript**. Supports cross‑browser testing, Codegen‑assisted script generation, data‑driven design with Faker.js, accessibility checks with axe‑core, and Excel‑based validations using SheetJS.

### Features
- Cross‑browser testing on Chromium, Firefox, WebKit.  
- TypeScript‑typed tests for better maintainability.  
- Page Object Model structure.  
- API‑level testing using Playwright’s `APIRequestContext`.  
- HTML reports for test execution and debugging.  
- Integration with Faker.js, axe‑core, and SheetJS.

### Installation
```bash
git clone <your-repo-url>
cd <your-project-folder>
npm install
npx playwright test
```

### Codegen – Record & Generate Tests
Use Playwright Codegen to rapidly generate test scripts from real user flows.

```bash
npx playwright codegen https://your-site.com
```

Workflow:
1. Run the command and perform key flows (login, registration, enrollment‑like forms).  
2. Copy the generated code from the Playwright Inspector.  
3. Paste into your TypeScript test file and enhance it with Faker‑based data and axe checks.

### Test Reports
```bash
npx playwright show-report
```

Includes:
- Test status and timing.  
- Screenshots and error logs.  
- CI/CD‑ready output for Azure DevOps, GitHub Actions, or Jenkins.

---

## Faker.js – Data‑Driven Testing

Faker.js generates realistic, varied test data (names, emails, phone numbers, addresses, etc.) that fits well with forms and Salesforce‑style contact/lead workflows.

### Installation
```bash
npm install @faker-js/faker --save-dev
```

### Example – Dynamic Parent / Child Registration
```ts
import { faker } from '@faker-js/faker';

// Generate realistic parent and child data
const parentFirstName = faker.person.firstName();
const parentLastName = faker.person.lastName();
const parentEmail = faker.internet.email();
const parentPhone = faker.phone.number();
const street = faker.location.streetAddress();
const city = faker.location.city();
const zipCode = faker.location.zipCode();
const childName = faker.person.firstName();
const randomNotes = faker.lorem.sentence();
```

You can plug this into Playwright tests for:
- Child care registration forms.  
- Salesforce‑integrated contact/lead creation flows.  

---

## axe‑core – Accessibility & Section 508 Testing

axe‑core automatically validates accessibility issues (missing labels, low contrast, improper ARIA, keyboard navigation) and supports Section 508 compliance efforts.

### Installation
```bash
npm install @axe-core/playwright --save-dev
```

### Example – Accessibility Scan
```ts
import { test, expect } from '@playwright/test';
import AxeBuilder from '@axe-core/playwright';

test('homepage accessibility scan', async ({ page }) => {
  await page.goto('https://your-childcare-site.com');

  const results = await new AxeBuilder({ page })
    .withTags(['wcag2a', 'wcag2aa'])
    .analyze();

  expect(results.violations).toEqual([]);
});
```

Use this pattern in:
- Child care enrollment pages.  
- Salesforce Experience Cloud or portal‑style sites.  

---

## SheetJS – Excel & Data Validation

SheetJS (xlsx) reads and validates Excel files programmatically. Useful for:
- Importing test data from spreadsheets.  
- Validating downloaded reports (attendance, billing, Salesforce exports).  
- Simulating 508‑style Excel checks (headers, alt text, structure).

### Installation
```bash
npm install xlsx
```

### Example – Validate Downloaded Excel Report
```ts
import * as XLSX from 'xlsx';

// Read Excel file
const workbook = XLSX.readFile('enrollment-export.xlsx');
const sheetName = workbook.SheetNames;
const sheet = workbook.Sheets[sheetName];

// Convert to JSON for validation
const data = XLSX.utils.sheet_to_json(sheet);
console.log(data.s
