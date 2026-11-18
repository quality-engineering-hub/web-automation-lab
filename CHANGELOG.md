
# Changelog

All notable changes to the Web Automation Lab are documented
in this file.

This project follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)
and [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

Changes that are under development and have not yet been
included in a published release.

### Added

- Initial Web Automation Lab repository structure.
- Framework directories for Playwright, Cypress and Selenium.
- Practice project directories for web application testing.
- Browser organisation for Chromium, Firefox and WebKit.
- Shared directories for fixtures, test data, utilities and reporting.
- Documentation directories for architecture, standards, setup and strategies.
- Repository formatting configuration through `.editorconfig`.
- Git file handling standards through `.gitattributes`.
- Ignore rules for generated files, dependencies and local secrets.
- Environment variable template through `.env.example`.

### Changed

- Not applicable.

### Deprecated

- Not applicable.

### Removed

- Not applicable.

### Fixed

- Not applicable.

### Security

- Added ignore rules to reduce the risk of committing local secrets and credentials.
- Established a foundation for secure contribution and testing practices.

---

## [0.1.0] - TBD

### Added

- Initial public repository release.
- Established the Web Automation Lab's purpose and scope.
- Defined the initial framework and browser organisation.
- Established foundational repository configuration.

---

## Change Categories

Changes should be grouped under the following headings:

| Category | Purpose |
|---|---|
| Added | New features and capabilities |
| Changed | Changes to existing functionality |
| Deprecated | Features scheduled for removal |
| Removed | Removed features or functionality |
| Fixed | Bug fixes and corrections |
| Security | Security improvements and vulnerability fixes |

## Versioning Policy

This project follows Semantic Versioning:

- MAJOR: Incompatible changes to established interfaces or behaviour.
- MINOR: New functionality introduced in a backwards-compatible manner.
- PATCH: Backwards-compatible bug fixes and improvements.

## Changelog Maintenance Rules

1. Every meaningful change should be documented.
2. Changes should initially be recorded under `Unreleased`.
3. Release entries should include the release version and date.
4. Entries should describe the impact of a change, not simply repeat commit messages.
5. Security-related changes should be documented without exposing sensitive vulnerability details.
6. Keep entries concise, clear and understandable to contributors.
