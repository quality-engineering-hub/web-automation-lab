
# Security Policy

## 1. Introduction

Quality Engineering Hub is committed to developing and maintaining
secure, reliable and responsible software quality engineering
resources.

The Web Automation Lab promotes secure software testing,
responsible automation, vulnerability awareness and good
engineering practices.

Security is an important part of software quality.

We take security vulnerabilities, accidental exposure of sensitive
information and unsafe implementations seriously.

This document explains how to report security vulnerabilities
and how security matters are handled within this repository.

---

## 2. Supported Versions

Security updates are prioritised for the latest maintained version
of the Web Automation Lab.

| Version | Security Support |
|---|---|
| Latest default branch | Supported |
| Previous releases | Best effort |
| Older or archived versions | Not guaranteed |

Contributors should use the latest maintained implementation
where practical.

Security fixes may not be backported to older versions unless
maintainers consider it necessary.

---

## 3. Reporting a Security Vulnerability

**Do not report security vulnerabilities through public GitHub
issues, discussions or pull requests.**

Public disclosure may expose systems, credentials, users or
other sensitive information.

For private vulnerability reporting, use GitHub's
**Report a vulnerability** feature if private vulnerability
reporting is enabled for this repository.

Alternatively, contact:

**Security contact:** [INSERT A MONITORED SECURITY EMAIL]

Only publish an email address that is controlled and regularly
monitored by the organisation maintainers.

### Information to Include

When reporting a vulnerability, provide as much of the following
information as safely possible:

- A clear description of the vulnerability.
- The affected repository, component or framework.
- The affected version or commit.
- Steps required to reproduce the issue.
- The potential security impact.
- Relevant logs or screenshots with sensitive information removed.
- A suggested remediation, if known.

Do not include live credentials, access tokens, private keys,
personal information or confidential production data.

---

## 4. Responsible Disclosure

We ask security researchers and contributors to:

- Report vulnerabilities privately.
- Avoid accessing, modifying or deleting other people's data.
- Avoid disrupting services or systems.
- Avoid testing against systems without authorisation.
- Avoid publishing vulnerability details before maintainers
  have had a reasonable opportunity to investigate.
- Share sufficient information to reproduce and understand
  the reported issue.

Do not perform destructive testing against infrastructure,
applications or services that you do not own or have explicit
permission to test.

Quality Engineering Hub does not authorise security testing
against third-party systems merely because they appear in
examples or documentation.

---

## 5. Vulnerability Handling Process

Security reports will be handled through the following process:

### Step 1: Acknowledgement

Maintainers will acknowledge receipt of a report when reasonably
possible.

### Step 2: Assessment

The report will be reviewed to determine:

- Whether the issue is reproducible.
- Which components are affected.
- The potential impact.
- The severity and urgency.
- Whether additional investigation is required.

### Step 3: Remediation

Where appropriate, maintainers will:

- Develop a security fix.
- Update affected dependencies.
- Improve configuration or implementation.
- Add regression tests.
- Document the remediation.

### Step 4: Verification

The proposed fix will be reviewed and tested to confirm that
the vulnerability has been addressed.

### Step 5: Disclosure

Maintainers will coordinate an appropriate disclosure after
the issue has been investigated and addressed where possible.

Public disclosure will avoid unnecessarily exposing sensitive
information.

---

## 6. Security Development Standards

All contributions should follow appropriate secure engineering
practices.

### 6.1 Secrets Management

Never commit:

- Passwords.
- API keys.
- Access tokens.
- Private SSH keys.
- Private certificates.
- Database credentials.
- Production authentication details.
- Cloud provider credentials.

Use environment variables and secure secret-management
mechanisms.

Use `.env.example` for placeholder configuration.

### 6.2 Dependency Management

Contributors should:

- Use trusted package sources.
- Avoid unnecessary dependencies.
- Keep dependencies reasonably up to date.
- Review dependency security advisories.
- Investigate known vulnerabilities.
- Avoid committing generated dependency directories.

### 6.3 Test Data Protection

Test data should not expose real personal or confidential
information.

Prefer:

- Synthetic test data.
- Anonymised datasets.
- Dedicated testing accounts.
- Non-production environments.
- Controlled test fixtures.

### 6.4 Browser Automation Security

Browser automation implementations should:

- Avoid storing credentials in source code.
- Protect authentication state files.
- Avoid exposing session cookies.
- Avoid committing browser profiles.
- Protect screenshots and execution traces.
- Use authorised test environments.

### 6.5 CI/CD Security

Automation workflows should:

- Use GitHub Actions secrets for sensitive values.
- Follow the principle of least privilege.
- Avoid exposing secrets in workflow logs.
- Review third-party GitHub Actions before use.
- Pin third-party actions to full commit SHAs where practical.
- Avoid granting unnecessary repository permissions.
- Protect sensitive deployment and testing environments.

### 6.6 Security Testing

Security testing examples should be performed only against
authorised applications and environments.

Security demonstrations must not encourage unauthorised access,
data theft, service disruption or other harmful activities.

---

## 7. Sensitive Information and Accidental Exposure

If sensitive information is accidentally committed:

1. Stop using the exposed credential immediately.
2. Revoke or rotate the affected credential.
3. Notify the repository maintainers privately.
4. Assess whether the credential or information was accessed.
5. Remove the exposed information from the repository history
   where appropriate.
6. Review relevant logs and systems.

Removing a secret from the latest commit does not guarantee
that it has been removed from Git history, forks, clones or
external caches.

Credential rotation is essential.

---

## 8. Security Tools and Automation

The Web Automation Lab may use security tools and practices such as:

- GitHub Dependabot.
- GitHub Secret Scanning.
- GitHub Code Scanning.
- OWASP ZAP.
- Trivy.
- Dependency vulnerability scanning.
- Static application security testing.
- Container security scanning.

The availability and use of these tools depend on repository
configuration, permissions and applicable GitHub features.

Security findings should be reviewed rather than automatically
treated as confirmed vulnerabilities.

---

## 9. Security Responsibilities

### Maintainers

Maintainers are responsible for:

- Reviewing private vulnerability reports.
- Assessing reported security issues.
- Coordinating remediation.
- Protecting confidential security information.
- Reviewing security-sensitive contributions.
- Communicating relevant security updates.

### Contributors

Contributors are responsible for:

- Following secure development practices.
- Protecting credentials and sensitive information.
- Reporting suspected vulnerabilities privately.
- Avoiding unauthorised testing.
- Reviewing security implications of their changes.

### Users

Users are responsible for:

- Reviewing configurations before using them.
- Protecting their local credentials.
- Using authorised testing environments.
- Keeping dependencies and tools updated.
- Understanding the limitations of demonstration code.

---

## 10. Scope and Limitations

This security policy applies to the Web Automation Lab repository
and its maintained examples and implementations.

It does not automatically extend authorisation to test:

- Third-party websites.
- External APIs.
- Production applications.
- Cloud infrastructure.
- Other GitHub repositories.
- Systems operated by other organisations.

The presence of an application in a testing example does not
constitute permission to conduct security testing against it.

---

## 11. Security Updates

Security-related changes may be communicated through:

- GitHub security advisories.
- Repository release notes.
- Changelog entries.
- Relevant documentation updates.

Sensitive vulnerability details will not be unnecessarily
included in public communications.

---

## 12. Contact

For security-related matters, use GitHub's private vulnerability
reporting feature where available.

Alternatively:

**Security contact:** [INSERT A MONITORED SECURITY EMAIL]

**Organisation:** Quality Engineering Hub

**Repository:** Web Automation Lab

**Repository URL:**
https://github.com/quality-engineering-hub/web-automation-lab

---

## Final Statement

Security is not an optional feature of software quality.

It is an engineering responsibility that must be considered
throughout design, implementation, testing, deployment and
maintenance.

Quality Engineering Hub encourages responsible security
research, practical security testing and continuous improvement.

**Build securely. Test responsibly. Protect what matters.**
