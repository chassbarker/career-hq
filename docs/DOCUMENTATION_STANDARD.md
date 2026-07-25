# Documentation Standard

| Property | Value |
|----------|-------|
| Document | Documentation Standard |
| Project | Career HQ |
| Document Version | 0.2.0 |
| Product Version | 0.2.0 |
| Status | Active |
| Owner | Chassidy Barker |
| Last Updated | July 24, 2026 |

---

# Overview

This document establishes the documentation standards used throughout the Career HQ project.

Its purpose is to ensure every document follows a consistent structure, writing style, formatting standard, and versioning strategy.

Consistent documentation improves readability, maintainability, and professionalism throughout the project.

---

# Documentation Goals

All project documentation should:

- Be accurate
- Be easy to read
- Remain current
- Be professionally formatted
- Be version controlled
- Grow alongside the application
- Reflect implemented functionality
- Clearly distinguish completed features from planned features

---

# Standard Document Structure

Unless a document requires a different format, all documentation should follow this structure:

```text
Title

Document Information

Overview

Main Content

Current Status

Revision History
```

---

# Document Information

Every document begins with the following information.

```markdown
| Property | Value |
|----------|-------|
| Document | Document Name |
| Project | Career HQ |
| Document Version | 0.2.0 |
| Product Version | 0.2.0 |
| Status | In Development |
| Owner | Chassidy Barker |
| Last Updated | July 24, 2026 |
```

---

# Document Status Values

Use only the following status values.

| Status | Meaning |
|----------|-------------------------------|
| Draft | Initial work in progress |
| In Development | Actively being developed |
| Active | Complete and actively maintained |
| Released | Final for the current product version |
| Archived | No longer maintained |

---

# Document Versioning

Documentation versions follow the product lifecycle.

Example:

| Product Version | Document Version |
|----------------|------------------|
| 0.2.0 | 0.2.0 |
| 0.3.0 | 0.3.0 |
| 0.4.0 | 0.4.0 |
| 1.0.0 | 1.0.0 |

Whenever a document is significantly updated:

- Update the Document Version.
- Update the Product Version if applicable.
- Update the Last Updated date.
- Add an entry to the Revision History.

---

# Writing Style

Documentation should:

- Use clear, professional language.
- Be concise while remaining descriptive.
- Avoid unnecessary jargon.
- Explain technical concepts when appropriate.
- Use consistent terminology throughout the project.

---

# Markdown Standards

Use:

- Heading hierarchy
- Tables for structured information
- Bullet lists for readability
- Code blocks for examples
- Horizontal rules between major sections

Avoid:

- Excessive formatting
- Large blocks of text without headings
- Inconsistent heading levels

---

# Headings

Recommended heading hierarchy:

```text
# Document Title

## Major Section

### Subsection

#### Optional Detail
```

Do not skip heading levels.

---

# Lists

Use unordered lists when order is not important.

Example:

- HTML
- CSS
- JavaScript

Use numbered lists for procedures.

Example:

1. Plan
2. Build
3. Test
4. Commit
5. Deploy

---

# Code Blocks

Always specify the language.

Example:

```html
<section>
```

```javascript
function initApp() {}
```

```sql
SELECT * FROM applications;
```

---

# Tables

Use tables for structured information.

Example:

| Property | Value |
|----------|-------|
| Project | Career HQ |

---

# Images

Future documentation images should:

- Use PNG format when possible.
- Be stored inside:

```text
screenshots/
```

Use descriptive filenames.

Example:

```text
dashboard-home.png

login-page.png

application-tracker.png
```

---

# Diagrams

Architecture diagrams should be:

- Clear
- Consistent
- Simple
- Updated when architecture changes

Future diagrams may include:

- System architecture
- Database relationships
- Authentication flow
- AWS architecture
- Application workflow

---

# Revision History

Every document should end with:

```markdown
# Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.2.0 | July 24, 2026 | Initial document |
```

Future revisions should be appended.

Example:

| Version | Date | Description |
|----------|------|-------------|
| 0.3.0 | August 18, 2026 | Updated for dashboard implementation |

---

# Current Status

## Implemented

- Documentation structure
- Versioning standard
- Metadata template
- Markdown formatting standard

## Planned

- Architecture diagram standards
- Screenshot standards
- Release documentation standards

---

# Related Documents

- Product Requirements
- System Architecture
- Database Design
- Security
- UI/UX Guidelines
- Development Roadmap
- Git Commit Guidelines
- Contributing Guide

---

# Revision History

| Version | Date | Description |
|----------|------|-------------|
| 0.2.0 | July 24, 2026 | Initial Documentation Standard |
