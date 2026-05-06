# Hi, I'm Veronica! 👋

I am a Results-driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise platforms. I specialize in building reliable test strategies that improve software quality, data integrity, and user experience.

---

## Skills

- **Testing Types:** QA Testing, Regression, Smoke, UAT, API Testing, End-to-End Testing, Exploratory Testing, Mobile Testing, UI/UX Testing, Compatibility Testing, Performance Testing, Accessibility Testing, Section 508 Testing
- **Automation & Testing Tools:** Playwright, Selenium, JMeter, Postman, axe-core, Faker.js, SheetJS, LoadRunner, BrowserStack, Charles Proxy
- **Programming & Scripting:** HTML, CSS, TypeScript, JavaScript, SQL
- **Databases:** MySQL, PostgreSQL, Cosmos DB, Data Validation & Verification
- **Platforms & DevOps:** Azure DevOps, CI/CD, Jenkins, GitHub, GitLab, SAP, Salesforce, Android Studio, Xcode
- **Project Management:** Jira, Confluence, Zephyr, Trello, SDLC, STLC, Defect Tracking, Agile/Scrum
- **Soft Skills:** Problem-solving, Critical Thinking, Analytical Thinking, Decision-making, Communication, Project Management

---

## Playwright Test Automation Framework

A scalable UI and API test automation framework built with Playwright and TypeScript. Designed for cross‑browser testing, CI/CD integration, and clear HTML reporting.

### Features
- Cross-browser testing on Chromium, Firefox, and WebKit.  
- UI and API test coverage.  
- Page Object Model structure for maintainable code.  
- HTML reports for test results.  
- CI/CD-ready configuration.

### Installation
```bash
git clone <your-repo-url>
cd <your-project-folder>
npm install
npx playwright test
```

### Codegen (Record & Generate Tests)
Use Playwright Codegen to record user actions and generate test scripts.

```bash
npx playwright codegen https://your-url-here.com
```

Workflow:
1. Run the command above and open the browser.  
2. Perform user actions (login, form fill, navigation).  
3. Copy the generated code from the Playwright Inspector.  
4. Paste into your test file and run.

### Test Reports
After test execution, open the HTML report:

```bash
npx playwright show-report
```

The report includes:
- Test pass/fail status and execution time.  
- Screenshots and error messages.  
- Step‑by‑step test details for debugging.

---

## Test Data Tools

### Faker.js – Dynamic Test Data
Generates realistic names, emails, addresses, and other values for more robust test cases.

**Installation**
```bash
npm install @faker-js/faker --save-dev
```

**Example**
```ts
import { faker } from '@faker-js/faker';

const firstName = faker.person.firstName();
const lastName = faker.person.lastName();
const email = faker.internet.email();
```

---

### axe-core – Accessibility Testing
Validates accessibility compliance (WCAG / Section 508) in web applications.

**Installation**
```bash
npm install @axe-core/playwright --save-dev
```

**Example**
```ts
import { test, expect } from '@playwright/test';
import AxeBuilder from '@axe-core/playwright';

test('homepage accessibility check', async ({ page }) => {
  await page.goto('https://example.com');
  const accessibilityScanResults = await new AxeBuilder({ page }).analyze();
  expect(accessibilityScanResults.violations).toEqual([]);
});
```

---

### SheetJS – Excel & Data Validation
Reads and validates Excel files for test data and report verification.

**Installation**
```bash
npm install xlsx
```

**Example**
```ts
import * as XLSX from 'xlsx';

const workbook = XLSX.readFile('test-data.xlsx');
const sheetName = workbook.SheetNames;
const sheet = workbook.Sheets[sheetName];
const data = XLSX.utils.sheet_to_json(sheet);
console.log(data);
```

---

## Summary

Results-driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise systems. Skilled in Playwright, Faker.js, axe-core, and SheetJS, with a strong focus on test data generation, accessibility validation, and end‑to‑end quality assurance in Agile environments.
