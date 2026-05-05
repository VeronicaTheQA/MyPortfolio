Hi, I’m Veronica! 👋
I’m a Results-driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise platforms. I specialize in building reliable test strategies that improve software quality, data integrity, and user experience. I work well in Agile teams and enjoy creating practical automation solutions that support faster, more stable releases.

Skills
Category	Skills
Testing Types	QA Testing, Regression, Smoke, UAT, API Testing, End-to-End Testing, Exploratory Testing, Mobile Testing, UI/UX Testing, Compatibility Testing, Performance Testing, Accessibility Testing, Section 508 Testing
Automation & Testing Tools	Playwright, Selenium, JMeter, Postman, axe-core, Faker.js, SheetJS, LoadRunner, BrowserStack, Charles Proxy
Programming & Scripting	HTML, CSS, TypeScript, JavaScript, SQL
Databases	MySQL, PostgreSQL, Cosmos DB, Data Validation & Verification
Platforms & DevOps	Azure DevOps, CI/CD, Jenkins, GitHub, GitLab, SAP, Salesforce, Android Studio, Xcode
Project Management	Jira, Confluence, Zephyr, Trello, SDLC, STLC, Defect Tracking, Agile/Scrum
Soft Skills	Problem-solving, Critical Thinking, Analytical Thinking, Decision-making, Communication, Project Management
My Projects
Playwright Automation Framework
A robust web automation framework built with Playwright and TypeScript for UI, API, and regression testing. This framework supports scalable test design, reusable page objects, and CI/CD integration.

Features
Cross-browser testing on Chromium, Firefox, and WebKit.

UI and API test coverage.

Page Object Model structure for maintainability.

CI/CD-ready setup for automated execution.

HTML reporting for test results.

Installation
bash
git clone <your-repo-url>
cd <your-project-folder>
npm install
npx playwright test
Generate Tests with Codegen
Playwright Codegen can record browser actions and generate test scripts automatically.

Run Codegen
bash
npx playwright codegen https://your-url-here.com
How it works
Open the website in the Codegen browser window.

Perform the actions you want to automate.

Copy the generated steps from the Playwright Inspector.

Paste them into your test file.

Run the test in headless mode to verify it works.

View Test Reports
Playwright generates an HTML report after test execution.

Open the report
bash
npx playwright show-report
Report output
Test status and execution time.

Passed, failed, and flaky tests.

Screenshots, traces, and videos if configured.

Step-by-step execution details for easier debugging.

Faker.js Test Data Generation
Faker.js is used to generate realistic test data such as names, emails, phone numbers, addresses, and other dynamic values. This helps reduce hardcoded data and makes tests more reusable.

Installation
bash
npm install @faker-js/faker --save-dev
Example Usage
ts
import { faker } from '@faker-js/faker';

const firstName = faker.person.firstName();
const lastName = faker.person.lastName();
const email = faker.internet.email();
axe-core Accessibility Testing
axe-core helps validate accessibility in web applications by identifying issues related to WCAG and Section 508 compliance. It is useful for checking keyboard navigation, color contrast, semantic structure, labels, and other accessibility concerns.

Installation
bash
npm install @axe-core/playwright --save-dev
Example Usage
ts
import { test, expect } from '@playwright/test';
import AxeBuilder from '@axe-core/playwright';

test('homepage accessibility check', async ({ page }) => {
  await page.goto('https://example.com');
  const accessibilityScanResults = await new AxeBuilder({ page }).analyze();
  expect(accessibilityScanResults.violations).toEqual([]);
});
SheetJS Data Validation
SheetJS is used to read, write, and validate Excel files during testing. It is helpful for test data management, spreadsheet verification, and file export validation.

Installation
bash
npm install xlsx
Example Usage
ts
import * as XLSX from 'xlsx';

const workbook = XLSX.readFile('test-data.xlsx');
const sheetName = workbook.SheetNames[0];
const sheet = workbook.Sheets[sheetName];
const data = XLSX.utils.sheet_to_json(sheet);
console.log(data);
Resume Summary
Results-driven QA Software Testing Analyst with experience in manual, automated, performance, and accessibility testing across web, mobile, API, and enterprise systems. Skilled in Playwright, Faker.js, axe-core, and SheetJS, with a strong focus on test data generation, accessibility validation, and end-to-end quality assurance in Agile environments.

Page Object Model
Page Object Model is used to keep automation code clean, reusable, and easy to maintain. It separates page locators and actions from test logic, which improves scalability and readability.

[
[

Playwright’s Codegen records browser interactions and generates test code, and the HTML reporter can be opened with npx playwright show-report after execution
