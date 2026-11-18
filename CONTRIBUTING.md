
# Contributing to the Web Automation Lab

Thank you for your interest in contributing to the Quality Engineering Hub
Web Automation Lab.

This project is an open engineering laboratory focused on practical
software quality engineering, web testing, test automation and
continuous improvement.

We welcome contributions from software testers, QA engineers,
automation engineers, software developers, security engineers,
students and anyone interested in improving software quality.

You do not need to be an expert to contribute.

What matters is a willingness to learn, share knowledge, follow
engineering standards and produce useful work.

---

## Table of Contents

1. Our Contribution Principles
2. Ways to Contribute
3. Before You Start
4. Repository Structure
5. Development Environment
6. Development Standards
7. Test Automation Standards
8. Documentation Standards
9. Reporting Issues
10. Submitting Contributions
11. Pull Request Requirements
12. Code Review Process
13. Security and Responsible Disclosure
14. Community Expectations
15. Getting Help

---

## 1. Our Contribution Principles

All contributions should support the following engineering principles:

- Quality: Build reliable and maintainable testing solutions.
- Clarity: Prefer understandable implementations over unnecessary complexity.
- Reusability: Build components that can be reused where appropriate.
- Reliability: Produce predictable and reproducible test results.
- Maintainability: Write code that other engineers can understand and improve.
- Evidence: Support technical claims with results, examples or documentation.
- Security: Protect credentials, personal information and sensitive data.
- Collaboration: Share knowledge and help other contributors grow.

Our objective is not simply to produce more automated tests.

Our objective is to improve how software quality is understood,
engineered, verified and demonstrated.

---

## 2. Ways to Contribute

There are several ways to participate.

### 2.1 Framework Development

Contribute to:

- Playwright automation.
- Cypress automation.
- Selenium automation.
- Framework architecture.
- Reusable test utilities.
- Page Object Model implementations.
- Test execution strategies.
- Browser compatibility.

### 2.2 Practice Projects

Contribute practical implementations demonstrating:

- Functional testing.
- Regression testing.
- End-to-end testing.
- Cross-browser testing.
- Form validation.
- Authentication testing.
- Navigation testing.
- Error handling.
- Accessibility testing.

### 2.3 Test Engineering

Help improve:

- Test case design.
- Test data management.
- Test isolation.
- Fixtures.
- Assertions.
- Test reporting.
- Failure analysis.
- Test reliability.

### 2.4 Performance and Reliability

Contribute examples covering:

- Response-time validation.
- Load testing.
- Performance baselines.
- Reliability testing.
- Execution monitoring.

### 2.5 Documentation

Documentation contributions are welcome, including:

- Setup guides.
- Architecture documents.
- Tutorials.
- Engineering standards.
- Troubleshooting guides.
- Practical examples.
- Learning resources.

### 2.6 Bug Fixes and Improvements

You can also:

- Fix existing defects.
- Improve code quality.
- Refactor difficult implementations.
- Improve test coverage.
- Resolve documentation errors.
- Improve CI/CD workflows.

---

## 3. Before You Start

Before contributing:

1. Read this document.
2. Read the repository README.
3. Review the project structure.
4. Check existing issues and pull requests.
5. Look for an existing implementation before creating another.
6. Open an issue if the proposed change is significant or introduces
   a new architectural direction.

For significant changes, discuss the proposed approach before
investing substantial implementation effort.

This helps prevent duplicated work and unnecessary rework.

---

## 4. Repository Structure

The Web Automation Lab uses a framework-oriented structure.

```text
web-automation-lab/
│
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
│
├── docs/
│   ├── architecture/
│   ├── standards/
│   ├── setup/
│   └── strategies/
│
├── frameworks/
│   ├── playwright/
│   ├── cypress/
│   └── selenium/
│
├── projects/
│   ├── saucedemo/
│   ├── demoqa/
│   ├── the-internet/
│   └── parabank/
│
├── browsers/
│   ├── chromium/
│   ├── firefox/
│   └── webkit/
│
├── tests/
│   ├── e2e/
│   ├── integration/
│   ├── fixtures/
│   └── support/
│
├── shared/
│   ├── fixtures/
│   ├── test-data/
│   ├── utilities/
│   └── reporting/
│
└── templates/
```

### Structural responsibilities

- frameworks/: Framework-specific implementations and configurations.
- projects/: Application-specific automation projects.
- browsers/: Browser compatibility strategies and documentation.
- tests/: Cross-framework validation and shared lab-level tests.
- shared/: Reusable resources where genuine cross-framework reuse is appropriate.
- docs/: Engineering documentation and standards.
- templates/: Reusable project and contribution templates.

Actual framework-specific test suites should normally remain
inside their respective framework directories.

Do not create unnecessary dependencies between Playwright,
Cypress and Selenium implementations.

---

## 5. Development Environment

Contributors should use supported versions of the relevant
frameworks and tools.

The project may use:

- Ubuntu Linux.
- Windows.
- macOS.
- Git and GitHub.
- Node.js and npm.
- Python.
- Java or C#.
- Playwright.
- Cypress.
- Selenium.
- Docker.
- GitHub Actions.

Refer to the relevant framework README for installation
instructions and supported versions.

### General setup

Clone the repository:

```bash
git clone https://github.com/quality-engineering-hub/web-automation-lab.git
```

Navigate into the project:

```bash
cd web-automation-lab
```

Create a working branch:

```bash
git switch -c feature/short-description
```

Use a branch name that communicates the purpose of the work.

Examples:

```text
feature/playwright-login-tests
feature/cypress-page-object-model
feature/selenium-browser-setup
fix/test-data-isolation
docs/update-setup-guide
```

---

## 6. Development Standards

### 6.1 General coding standards

Contributions should:

- Use clear and descriptive names.
- Follow the conventions of the selected programming language.
- Avoid unnecessary duplication.
- Keep functions and classes focused.
- Handle errors appropriately.
- Avoid hardcoded credentials and secrets.
- Include comments where they explain important decisions.
- Remove unused code and debugging statements.
- Avoid introducing unnecessary dependencies.

### 6.2 Formatting

Follow the repository formatting standards defined in:

- `.editorconfig`
- `.gitattributes`
- `.gitignore`

Use the relevant formatter and linter for the framework
being modified.

### 6.3 Configuration

Keep configuration separate from implementation where appropriate.

Prefer environment variables for environment-specific settings.

Do not commit:

- Passwords.
- Access tokens.
- API keys.
- Private certificates.
- Production credentials.
- Personal information.

Use `.env.example` for documented configuration placeholders.

---

## 7. Test Automation Standards

Automated tests should be reliable, understandable and maintainable.

### 7.1 Test design

Each test should have:

- A clear purpose.
- A meaningful test name.
- Defined preconditions where necessary.
- Predictable test data.
- Appropriate assertions.
- Clear failure information.

### 7.2 Test independence

Tests should not depend unnecessarily on the execution order
of other tests.

Where possible:

- Isolate test data.
- Reset application state.
- Avoid shared mutable state.
- Avoid relying on previously executed tests.
- Make tests reproducible.

### 7.3 Selectors

Prefer stable selectors.

Examples include:

- Accessible roles.
- Accessible names.
- Labels.
- Stable test identifiers.

Avoid relying unnecessarily on:

- Fragile CSS selectors.
- Dynamic element identifiers.
- Deep DOM structures.
- Unstable positional selectors.

### 7.4 Wait strategies

Prefer condition-based waits over arbitrary fixed delays.

Avoid using unnecessary hardcoded sleeps to compensate for
poor synchronisation.

### 7.5 Assertions

Assertions should verify meaningful application behaviour.

Avoid assertions that only confirm an element exists when
the actual requirement concerns a specific business outcome.

### 7.6 Test reporting

Where appropriate, provide:

- Execution status.
- Failure details.
- Relevant error messages.
- Screenshots or traces.
- Browser and environment information.

Do not publish sensitive information in test reports.

---

## 8. Documentation Standards

Documentation is part of the implementation.

Contributions that introduce functionality should include
appropriate documentation.

Documentation should explain:

- What the implementation does.
- Why it exists.
- How to install or configure it.
- How to execute it.
- How to interpret its results.
- Known limitations.

Use Markdown for repository documentation.

Prefer practical examples over lengthy theoretical explanations.

Keep documentation accurate as implementations evolve.

---

## 9. Reporting Issues

Before creating an issue, search existing issues to avoid
duplicates.

When reporting a defect, include:

- A clear title.
- A description of the problem.
- Steps to reproduce.
- Expected behaviour.
- Actual behaviour.
- Relevant framework and tool versions.
- Operating system and browser information.
- Error messages or sanitised screenshots where useful.

For feature requests, explain:

- The problem being addressed.
- The proposed capability.
- Why it would be useful.
- Possible implementation considerations.

Do not include credentials, personal data or confidential
application information.

---

## 10. Submitting Contributions

Follow this workflow:

### Step 1: Fork the repository

Fork the repository into your GitHub account if you are
contributing from outside the organisation.

### Step 2: Clone your fork

```bash
git clone https://github.com/YOUR-USERNAME/web-automation-lab.git
cd web-automation-lab
```

### Step 3: Configure the upstream repository

```bash
git remote add upstream https://github.com/quality-engineering-hub/web-automation-lab.git
```

### Step 4: Create a feature branch

```bash
git switch -c feature/your-feature-name
```

### Step 5: Implement your changes

Make focused changes that address the intended issue or feature.

### Step 6: Run relevant checks

Run the appropriate tests, formatting tools and validation
commands for the framework you changed.

### Step 7: Review your changes

```bash
git status
git diff
```

Ensure that you have not included:

- Unrelated changes.
- Generated dependencies.
- Temporary files.
- Secrets or credentials.
- Unnecessary test artifacts.

### Step 8: Commit your changes

Use a clear commit message.

Examples:

```bash
git commit -m "feat: add Playwright login tests"
git commit -m "fix: improve Cypress test isolation"
git commit -m "docs: update Selenium setup guide"
git commit -m "test: add browser compatibility coverage"
```

### Step 9: Push your branch

```bash
git push origin feature/your-feature-name
```

### Step 10: Open a pull request

Submit a pull request against the original repository's
default branch.

Explain what changed, why it changed and how it was tested.

---

## 11. Pull Request Requirements

Every pull request should:

- Have a clear and descriptive title.
- Explain the problem being addressed.
- Describe the implementation.
- Reference a related issue where applicable.
- Include relevant tests.
- Include documentation updates where necessary.
- Pass applicable automated checks.
- Avoid unrelated changes.
- Contain no secrets or confidential information.

### Pull request description template

```markdown
## Summary

Describe the change.

## Problem

Explain the problem being addressed.

## Implementation

Describe what was implemented.

## Testing

Explain which tests and checks were performed.

## Evidence

Include relevant sanitised screenshots, reports or execution results.

## Checklist

- [ ] Changes follow repository standards.
- [ ] Relevant tests have been executed.
- [ ] New functionality includes appropriate tests.
- [ ] Documentation has been updated.
- [ ] No secrets or sensitive information are included.
- [ ] Changes are focused and ready for review.
```

---

## 12. Code Review Process

Pull requests may be reviewed for:

- Correctness.
- Maintainability.
- Readability.
- Test reliability.
- Test coverage.
- Architecture.
- Security.
- Documentation.
- Compatibility with existing implementations.

Review feedback should be constructive and technically justified.

Contributors are expected to respond to reasonable review
comments and make necessary improvements.

Approval and merging are controlled by repository maintainers.

Submitting a pull request does not guarantee acceptance.

---

## 13. Security and Responsible Disclosure

Security issues should not be reported through public GitHub
issues when doing so could expose a vulnerability.

Follow the instructions in `SECURITY.md`.

Never commit:

- Real credentials.
- Access tokens.
- Private keys.
- Production data.
- Confidential customer information.

Use authorised testing environments and applications.

Do not conduct unauthorised security testing against systems
you do not own or have permission to test.

---

## 14. Community Expectations

All contributors must follow the organisation's
[Code of Conduct](CODE_OF_CONDUCT.md).

We encourage:

- Professional communication.
- Constructive technical discussions.
- Respectful disagreements.
- Knowledge sharing.
- Accountability.
- Continuous learning.

Technical excellence and professional conduct should
go hand in hand.

---

## 15. Getting Help

If you need assistance:

1. Read the repository README.
2. Review the documentation in `docs/`.
3. Search existing GitHub issues and discussions.
4. Open a question or discussion where available.
5. Clearly explain what you are trying to achieve and
   where you are experiencing difficulty.

When requesting technical help, provide enough context
for another engineer to understand the problem.

---

## Final Note

Quality Engineering Hub is a collaborative engineering
laboratory.

Every useful contribution, whether it is a framework,
test scenario, defect fix, technical explanation or
documentation improvement, helps strengthen the community.

We value practical engineering, clear thinking,
reproducible results and a willingness to improve.

Thank you for helping us build better software quality
engineering practices.

**Automate. Validate. Secure. Perform.**
