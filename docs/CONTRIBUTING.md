# Contributing to Career HQ

Thank you for your interest in contributing to Career HQ.

Career HQ is currently a personal portfolio project developed and maintained by **Chassidy Barker**. While external contributions are not currently accepted, this document defines the development standards and workflow used throughout the project.

---

# Development Workflow

Every feature follows the same process:

1. Plan the feature.
2. Update project documentation if necessary.
3. Implement the feature.
4. Test functionality and responsiveness.
5. Commit changes using meaningful commit messages.
6. Update the changelog when appropriate.
7. Push changes to GitHub.

---

# Repository Structure

```
career-hq/
│
├── assets/
├── css/
├── database/
├── demo/
├── docs/
├── js/
├── pages/
├── screenshots/
│
├── index.html
├── README.md
├── CHANGELOG.md
└── LICENSE
```

---

# Branch Naming Convention

Future development should use descriptive branch names.

Examples:

```
feature/dashboard
feature/authentication
feature/job-applications
feature/resume-hq
feature/interview-hq

bugfix/mobile-navigation
bugfix/login

docs/readme
docs/security
```

---

# Commit Message Convention

Career HQ follows conventional commit messages.

Examples:

```
feat: add dashboard layout

fix: correct mobile navigation

docs: update system architecture

style: improve hero spacing

refactor: simplify dashboard components

test: add authentication tests

chore: update project dependencies
```

Each commit should represent one logical change.

---

# Coding Standards

- Use semantic HTML5 elements.
- Follow accessibility best practices (WCAG 2.2 AA).
- Write clean, readable, and maintainable code.
- Prefer reusable components and consistent naming.
- Keep JavaScript modular and organized.
- Use descriptive variable and function names.
- Avoid unused code and commented-out code.

---

# Testing Checklist

Before committing changes:

- Verify functionality.
- Test responsive layouts.
- Check accessibility where applicable.
- Test in multiple browsers when possible.
- Confirm GitHub Pages still builds correctly.

---

# Documentation

Project documentation should remain synchronized with development.

When appropriate, update:

- README.md
- CHANGELOG.md
- ROADMAP.md
- PRODUCT_REQUIREMENTS.md
- SYSTEM_ARCHITECTURE.md
- DATABASE_DESIGN.md
- SECURITY.md
- UI_UX_GUIDELINES.md

---

# License

This project is licensed under the MIT License.

See the LICENSE file for details.
