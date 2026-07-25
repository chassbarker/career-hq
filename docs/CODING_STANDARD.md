# Coding Standard

| Property         | Value            |
| ---------------- | ---------------- |
| Document         | Coding Standard  |
| Project          | Career HQ        |
| Document Version | 0.2.0            |
| Product Version  | 0.2.0            |
| Status           | Active           |
| Owner            | Chassidy Barker  |
| Last Updated     | July 24, 2026    |

---

## Overview

This document defines the coding standards used throughout the Career HQ project.

The purpose of these standards is to maintain consistent, readable, secure, and maintainable code while following modern web development and software engineering best practices.

These standards apply to all HTML, CSS, JavaScript, SQL, and future cloud-based development.

---

## Development Principles

Career HQ is built using the following principles:

- Write readable code before clever code.
- Keep files organized and maintainable.
- Prioritize accessibility.
- Build mobile-first.
- Design reusable components.
- Follow security best practices.
- Optimize for performance.
- Document significant changes.

---

## Project Structure

```text
career-hq/
│
├── assets/
│   ├── icons/
│   └── images/
│
├── css/
│   └── style.css
│
├── js/
│   └── app.js
│
├── pages/
├── database/
├── docs/
├── screenshots/
├── demo/
│
├── index.html
├── README.md
├── CHANGELOG.md
└── LICENSE
```

Every file should have a clear purpose.

---

## HTML Standards

Use semantic HTML whenever possible.

Preferred elements include:

- header
- nav
- main
- section
- article
- aside
- footer
- button

Avoid unnecessary `<div>` elements when semantic elements are more appropriate.

## HTML Accessibility

Every page should include:

- Proper heading hierarchy
- Alt text for images
- ARIA labels when appropriate
- Keyboard accessibility
- Skip navigation link
- Descriptive link text

---

## CSS Standards

Career HQ uses a mobile-first responsive design approach.

Guidelines:

- Organize styles by section.
- Group related rules together.
- Use CSS custom properties.
- Avoid duplicate styles.
- Keep selectors readable.
- Prefer Flexbox and Grid.
- Minimize specificity conflicts.

Example:

```css
.hero {
}

.hero-title {
}

.hero-description {
}
```

---

## JavaScript Standards

JavaScript should be:

- Modular
- Readable
- Well organized
- Reusable

Use:

- const by default
- let only when reassignment is required

Avoid:

- Global variables
- Duplicate functions
- Magic numbers
- Unused code

Functions should perform one responsibility.

Example:

```javascript
function initializeNavigation() {

}

function toggleMenu() {

}
```

---

## Naming Conventions

Use descriptive names.

Good

```text
applicationCard

dashboardStatistics

interviewReminder
```

Avoid

```text
app1

temp

data

test
```

---

## File Naming

Use lowercase file names.

Examples

```text
style.css

app.js

dashboard.html

security.md
```

Use hyphens when appropriate.

Example

```text
job-applications.html
```

---

## Folder Organization

Files should remain organized by purpose.

Example

```text
assets/

css/

database/

docs/

js/

pages/

screenshots/
```

Avoid placing unrelated files in the project root.

---

## Comments

Comments should explain **why**, not **what**.

Good

```javascript
// Close the mobile navigation after selecting a menu item.
```

Avoid

```javascript
// Increment i.
```

---

## Performance

Career HQ should:

- Minimize unnecessary JavaScript
- Reduce duplicate CSS
- Optimize images
- Use lazy loading where appropriate
- Keep pages lightweight

---

## Security

Never expose:

- API keys
- Service role keys
- Passwords
- Secrets

Use environment variables whenever possible.

Validate user input.

Escape output where appropriate.

Follow the Principle of Least Privilege.

---

## Accessibility

Career HQ aims to meet WCAG 2.2 AA.

Requirements include:

- Keyboard navigation
- Color contrast
- Screen reader compatibility
- Focus indicators
- Responsive layouts

Accessibility is considered throughout development rather than added afterward.

---

## Responsive Design

Design for:

- Mobile
- Tablet
- Laptop
- Desktop

Layouts should adapt without breaking functionality.

---

## Version Control

Development follows:

- Conventional Commits
- GitHub Flow
- Semantic Versioning

One logical change should be committed at a time.

---

## Testing

Before committing:

- Verify functionality.
- Test responsive layouts.
- Check accessibility.
- Test navigation.
- Confirm GitHub Pages builds correctly.

---

## AI-Assisted Development

AI tools may be used to:

- Brainstorm ideas
- Review code
- Explain concepts
- Improve documentation

The developer is responsible for:

- Understanding generated code
- Testing all functionality
- Verifying correctness
- Making final implementation decisions

AI-generated code should never be copied without review.

---

## Future Standards

As Career HQ evolves, this document may expand to include:

- TypeScript standards
- React standards
- API design guidelines
- SQL conventions
- AWS coding standards
- Automated testing
- CI/CD workflows

---

## Current Status

### Implemented

- HTML standards
- CSS standards
- JavaScript standards
- Accessibility guidelines
- Responsive design standards
- Version control practices

## Planned

- TypeScript standards
- React standards
- API development standards
- Cloud development standards
- Automated testing standards

---

## Revision History

| Version | Date          | Description             |
| ------- | ------------- | ----------------------- |
| 0.2.0   | July 24, 2026 | Initial Coding Standard |
