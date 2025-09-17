
# Hi, I'm Veronica! 👋

I am a Results-driven QA Software Testing Analyst with expertise in manual, automated, and performance testing across web, mobile, and API platforms. I am passionate about designing comprehensive test strategies that ensure software quality, security, and an exceptional user experience. My collaborative approach within Agile teams has consistently led to increased efficiency and higher customer satisfaction.

| Category | Skills |
| :--- | :--- |
| **Testing Types** | QA Testing, Regression, Smoke, UAT, API Testing, End-to-End, Exploratory, Mobile App, UI/UX, Compatibility, Performance![Playwright](https://img.shields.io/badge/Playwright-Informational?style=flat&logo=playwright&logoColor=white)
| **Programming & Scripting** | HTML, CSS, TypeScript |
| **Databases** | MySQL, PostgreSQL, Cosmos DB, Data Validation & Verification |
| **API Tools** | Postman, REST API, Charles Proxy |
| **Platforms & DevOps** | Azure DevOps, CI/CD, Jenkins, GitHub, GitLab, SAP, Salesforce, Android Studio, Xcode |
| **Project Management** | Jira, Confluence, Zephyr, Trello, SDLC, STLC, Defect Tracking, Agile/Scrum |
| **Soft Skills** | Problem-solving, Critical Thinking, Analytical, Decision-making, Communication, Project Management |

# My Projects

# Automation Testing with Playwright's Codegen Tool

1. Click in the tests folder, then click on new file which you will see when hovering over the root folder's name
2. In the terminal write the following script: npx playwright codegen, followed by the website link example in the video: npx playwright codegen (LINK)

Websites you can use for end to end testing

https://the-internet.heroukapp.com  
https://www.saucedemo/v1/

3. Log in as a user would do, all actions are being recorded
4. On the playwright inspector click on the copy to copy all actions, paste it into the playwright test file
5. Click on the green checkmark to run the test in headless mode, meaning it is running in the background

# Framework for theinternethero website

# Playwright Web Automation Framework

[![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)](https://playwright.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)

A robust and scalable test automation framework built with Playwright and TypeScript. Demonstrates best practices for UI testing, API testing, and visual regression.

## 🚀 Features

- **Cross-Browser Testing**: Tests run on Chromium, Firefox, and WebKit.
- **API Testing**: Examples of REST API request validation.
- **Visual Regression Testing**: Screenshot comparisons to catch UI bugs.
- **Parallel Execution**: Tests are configured to run in parallel for speed.
- **CI/CD Integration**: Ready-to-use GitHub Actions workflow.
- **HTML Reports**: Detailed and interactive post-execution reports.

## 📁 Project Structure

```
playwright-framework/
├── tests/
│   ├── ui/                 # UI tests
│   ├── api/                # API tests
│   └── visual-regression/  # Visual tests
├── pages/                  # Page Object Model classes
├── helpers/                # Reusable helper functions
├── fixtures/               # Test fixtures for setup/teardown
└── playwright.config.ts    # Main configuration file
```

## 🛠️ Installation & Run

1.  Clone the repo: `git clone <your-repo-url>`
2.  Install dependencies: `npm install`
3.  Run tests: `npx playwright test`
4.  Open HTML report: `npx playwright show-report`


