# Hi, I'm Veronica! 👋

I am a Results‑driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise platforms. I specialize in building robust, maintainable test automation that supports data‑driven testing, accessibility compliance, and smooth integration with Salesforce and backend systems.

---

## Skills

- **Testing Types:** QA Testing, Regression, Smoke, UAT, API Testing, End‑to‑End Testing, Exploratory Testing, Mobile Testing, UI/UX Testing, Compatibility Testing, Performance Testing, Accessibility Testing, Section 508 Testing
- **Automation & Testing Tools:** Playwright, Selenium, JMeter, Postman, axe‑core, Faker.js, SheetJS, LoadRunner, BrowserStack, Charles Proxy
- **Languages & Scripting:** HTML, CSS, TypeScript, JavaScript, SQL
- **Databases:** MySQL, PostgreSQL, Cosmos DB, Data Validation & Verification
- **Platforms & DevOps:** Azure DevOps, CI/CD, Jenkins, GitHub, GitLab, SAP, Salesforce, Android Studio, Xcode
- **Project Management:** Jira, Confluence, Zephyr, Trello, SDLC, STLC, Defect Tracking, Agile/Scrum
- **Soft Skills:** Problem‑solving, Critical Thinking, Analytical Thinking, Decision‑making, Communication, Project Management

---

## Playwright Test Automation Framework

A scalable Playwright + TypeScript framework for UI, API, and accessibility‑aware testing. Designed for cross‑browser execution, CI/CD integration, Codegen‑assisted test creation, and clear HTML reporting.

### Features
- Cross‑browser testing on Chromium, Firefox, WebKit.  
- UI and API checks.  
- Page Object Model structure.  
- Test data generation with Faker.js.  
- Accessibility scans with axe‑core.  
- HTML reports for test execution and debugging.

### Installation
```bash
git clone <your-repo-url>
cd <your-project-folder>
npm install
npx playwright test
```

### Codegen – Record & Generate Tests
Use `npx playwright codegen` to rapidly generate test scripts from real user actions.

```bash
npx playwright codegen https://example.com
```

Workflow:
1. Run the command and open the browser window.  
2. Perform key user flows (login, form fill, navigation, enrollment‑like workflows as in child care sites).  
3. Copy the code from the Playwright Inspector.  
4. Paste into a test file and refine (add waits, assertions, Faker‑generated data, axe scans).

### Test Reports
After running tests, open the HTML report:

```bash
npx playwright show-report
```

The report includes:
- Test pass/fail status and execution time.  
- Screenshots and error logs.  
- Step‑by‑step execution for fast debugging.  
- CI/CD‑ready output compatible with pipelines on Azure DevOps or GitHub Actions.

---

## Faker.js – Smarter Test Data

Faker.js generates realistic, varied test data (names, emails, phone numbers, addresses, IDs, etc.), which helps avoid hardcoded values and supports data‑driven test design for web forms and Salesforce‑integrated workflows.

### Why Use Faker.js?
- Reduces tedious data maintenance.  
- Simulates real‑world user inputs (e.g., parent or caregiver details).  
- Helps test edge cases and validation rules (required fields, length limits, email formats).

### Installation
```bash
npm install @faker-js/faker --save-dev
```

### Example – Child Care / Salesforce‑style Form
```ts
import { faker } from '@faker-js/faker';

// Generate parent/caregiver information
const parentFirstName = faker.person.firstName();
const parentLastName = faker.person.lastName();
const parentEmail = faker.internet.email();
const parentPhone = faker.phone.number();
const street = faker.location.streetAddress();
const city = faker.location.city();
const zipCode = faker.location.zipCode();
const childName = faker.person.firstName();

// Use in Playwright test (pseudocode)
// await page.fill('input#parentName', `${parentFirstName} ${parentLastName}`);
// await page.fill('input#email', parentEmail);
// await page.fill('input#phone', parentPhone);
// await page.selectOption('select#childAge', '3');
// await page.click('button#submit');
```

This pattern is useful for:
- Parent registration forms.  
- Salesforce‑integrated contact or lead creation.  
- Multi‑record, data‑driven test scenarios.

---

## axe‑core – Accessibility & Section 508 Testing

axe‑core is an accessibility engine that automatically checks for WCAG‑compliant issues such as missing labels, low contrast, incorrect ARIA usage, and keyboard‑navigation problems. It is ideal for verifying compliance with Section 508 requirements on web applications.

### Why Use axe‑core?
- Automated accessibility checks in Playwright test suites.  
- Consistent scanning across pages and components.  
- Helps catch issues before users or auditors notice them.  
- Works well with single‑page applications and form‑heavy workflows (e.g., child care enrollment).

### Installation
```bash
npm install @axe-core/playwright --save-dev
```

### Example – Child Care Website Scan
```ts
import { test, expect } from '@playwright/test';
import AxeBuilder from '@axe-core/playwright';

test('child care homepage accessibility', async ({ page }) => {
  await page.goto('https://your-childcare-site.com');

  const results = await new AxeBuilder({ page })
    .withTags(['wcag2a', 'wcag2aa'])
    .analyze();

  expect(results.violations).toEqual([]);
  // Optionally log or store accessibility results for audit purposes
});
```

You can extend this to:
- Scan specific regions (e.g., enrollment form only).  
- Add accessibility checks into CI pipelines alongside UI tests.  

---

## SheetJS – Excel Data & Section 508‑style Validation

SheetJS (xlsx) reads, writes, and validates Excel files programmatically. It is useful for:
- Importing test data from spreadsheets into test runs.  
- Verifying downloaded reports or exports (e.g., attendance lists, billing extracts, or Salesforce‑exported CSV/Excel data).  
- Section 508–style checks on exported Excel files (structure, headers, alt text, and readability).

### Why Use SheetJS?
- Fast, scriptable Excel parsing without manual inspection.  
- Integrates cleanly with Playwright and Node for headless automation.  
- Enables automated checks on data‑driven test sets and reports.

### Installation
```bash
npm install xlsx
```

### Example – Validate Downloaded Excel Report
```ts
import * as XLSX from 'xlsx';

// Read test‑data or downloaded report
const workbook = XLSX.readFile('enrollment-export.xlsx');
const sheetName = workbook.SheetNames;
const sheet = workbook.Sheets[sheetName];

// Convert to JSON for easy validation
const data = XLSX.utils.sheet_to_json(sheet);
console.log(data.slice(0, 3)); // inspect first three rows

// Basic validation pattern (customize for your schema)
for (const row of data) {
  if (!row['Parent Email'] || !row['Child Name']) {
    throw new Error('Missing required fields in Excel export');
  }
}
```

### Example – Playwright + SheetJS (Headless Browser Export)
You can also combine Playwright and SheetJS in headless workflows:
- Use Playwright to log into a child care portal and download an Excel report.  
- Use SheetJS to validate the file contents (structure, column names, data integrity), simulating a QA‑focused audit.

---

## Summary

Results‑driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise systems. Skilled in Playwright, Faker.js, axe‑core, and SheetJS, with a strong focus on data‑driven testing, accessibility validation, and end‑to‑end quality assurance in Agile environments.
