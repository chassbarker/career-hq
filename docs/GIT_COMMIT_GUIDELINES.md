# Git Commit Guidelines

| Property | Value |
| -------- | ----- |
| Document | Git Commit Guidelines |
| Project | Career HQ |
| Document Version | 0.2.0 |
| Product Version | 0.2.0 |
| Status | Active |
| Author | Chassidy Barker |
| Last Updated | July 2026 |

---

Career HQ follows the Conventional Commits specification to create a clear, organized, and professional Git history.

## Commit Format

Every commit should include:

- A concise title
- A descriptive body explaining the changes

Example:

git commit -m "feat: add dashboard layout" -m "

- Create responsive dashboard layout
- Add sidebar navigation
- Add dashboard cards
- Prepare dashboard for authentication integration

"

---

## Commit Types

### feat

A new feature.

Examples

feat: add dashboard layout

feat: implement authentication

feat: create Resume HQ

---

## fix

A bug fix.

Examples

fix: correct mobile navigation

fix: resolve login validation

---

## docs

Documentation changes.

Examples

docs: update README

docs: add system architecture

docs: create security documentation

---

## style

Visual or formatting improvements that do not change functionality.

Examples

style: improve landing page spacing

style: update button styling

---

## refactor

Code improvements that do not change behavior.

Examples

refactor: simplify dashboard components

refactor: organize JavaScript modules

---

## test

Testing additions or improvements.

Examples

test: add authentication tests

test: improve form validation tests

---

## chore

Maintenance tasks.

Examples

chore: update dependencies

chore: configure GitHub Pages

---

## Commit Message Guidelines

Good

feat: add job application tracker

Bad

updated stuff

fixed things

changes

---

## Commit Body Guidelines

The commit body should summarize the major changes.

Example

git commit -m "feat: add Resume HQ" -m "

- Create resume management page
- Add resume version tracking
- Prepare secure file upload support
- Connect navigation links

"

---

## General Rules

- One logical change per commit.
- Keep commit titles under 72 characters when practical.
- Use the imperative mood ("add", "update", "fix"), not past tense.
- Test changes before committing.
- Update documentation when features change.
- Update CHANGELOG.md for significant releases.
- Push only after verifying the project builds successfully.

---

## Career HQ Workflow

1. Plan the feature.
2. Update documentation.
3. Implement the feature.
4. Test the feature.
5. Commit using Conventional Commits.
6. Push to GitHub.
7. Update the changelog if applicable.

This workflow is used throughout the Career HQ project to maintain a clean, professional development history.
