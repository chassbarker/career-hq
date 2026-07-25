# Career HQ

**An AI-Powered Career Management Platform**

Career HQ is a cloud-native, AI-powered career management platform designed to help students and early-career professionals organize every part of their job search in one secure and accessible place.

The platform brings job applications, resume versions, interview preparation, certifications, portfolio projects, salary research, networking, follow-up tasks, and long-term career goals into one centralized dashboard. Its purpose is to reduce overwhelm, make important information easier to manage, and help users clearly identify their next step.

Career HQ is my flagship portfolio project and reflects the skills I have developed while studying cloud computing. Through this project, I am applying full-stack development, cloud architecture, AWS integration, DevOps practices, database design, authentication, security, accessibility, and AI-assisted workflows to solve a real-world problem.

The project is being developed in phases, beginning with a responsive frontend and expanding into a secure full-stack application with Supabase, PostgreSQL, AWS services, automation, and future AI features.

## Live Demo

[View Career HQ](https://chassbarker.github.io/career-hq/)

> Career HQ is currently in active development. Features will be added in stages as the project progresses.

## Project Purpose

Students and early-career professionals often manage resumes, job applications, interview notes, certifications, projects, and follow-up tasks across several disconnected tools.

Career HQ brings these activities into one organized workflow that helps users:

* Keep career information in one place
* Track job applications from discovery through final outcome
* Save the exact resume and cover letter submitted for each position
* Research salary before applying or interviewing
* Prepare for interviews using the job description and submitted resume
* Track certifications, schoolwork, projects, and professional accomplishments
* Record follow-up actions and lessons learned
* Focus on clear, manageable next steps

## Target Users

Career HQ is designed for:

* College students approaching graduation
* Career changers entering technology
* Early-career cloud, AI, DevOps, and software professionals
* Users who benefit from visual organization and smaller next steps
* Job seekers managing multiple resumes and applications

## Planned Features

### Career Dashboard

* Top three daily priorities
* Upcoming interviews
* Application deadlines
* Follow-up reminders
* Weekly progress
* Quick capture area

### Job Application Tracker

* Company and position information
* Application status
* Posting link and saved job description
* Date found and date applied
* Recruiter or hiring contact
* Next action and due date
* Interview details
* Final outcome
* Lessons learned

### Resume Manager

* Master resume
* Cloud resume
* DevOps resume
* AI and machine-learning resume
* Web and software resume
* Handshake resume
* LinkedIn resume
* Submitted resume archive
* Resume revision history

### Interview HQ

* Company research
* Job-description analysis
* Behavioral interview questions
* STAR story preparation
* Technical study topics
* Project talking points
* Questions to ask interviewers
* Interview notes
* Post-interview reflection

### Salary Research

* Listed salary range
* Estimated market range
* Target salary
* Private minimum salary
* Hourly equivalent
* Total compensation review
* Research sources
* Salary follow-up reminders

### Email Center

* Interview confirmation
* Rescheduling messages
* Thank-you emails
* Follow-up emails
* Networking messages
* Offer acceptance
* Offer negotiation
* Offer decline
* Rejection response

### Projects and School Hub

* Coursework
* AWS labs
* Cloud projects
* AI and machine-learning projects
* GitHub repositories
* Architecture notes
* Screenshots
* Testing evidence
* Portfolio descriptions
* Lessons learned

### Certifications and Credentials

* Certification name
* Issuing organization
* Issue date
* Credly link
* Skills demonstrated
* Supporting evidence
* Renewal or expiration information

## Planned AI Features

Future AI-assisted features may include:

* Resume-to-job matching
* Suggested resume keywords
* Interview-question generation
* Personalized interview preparation
* Company research checklists
* STAR response coaching
* Salary research assistance
* Follow-up email drafting
* Career task prioritization
* Project description generation

AI-generated content will require user review before it is saved or used.

## Technology Stack

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend and Database

* Supabase
* PostgreSQL
* Supabase Authentication
* Row Level Security
* Supabase Storage

### Cloud and Hosting

* GitHub Pages
* Amazon Web Services planned integrations

### DevOps

* Git
* GitHub
* GitHub Projects
* GitHub Issues
* GitHub Actions
* CI/CD workflows

### Planned AWS Integrations

* Amazon S3 for document storage and backups
* AWS Lambda for automation
* Amazon EventBridge for scheduled reminders
* Amazon SES for email notifications
* Amazon CloudWatch for monitoring and logs
* Amazon Bedrock for future AI features

## Architecture Strategy

Career HQ will be built incrementally.

### Phase 1: Frontend Prototype

* HTML
* CSS
* JavaScript
* Sample data or local storage
* GitHub Pages deployment

### Phase 2: Secure Full-Stack Application

* Supabase authentication
* PostgreSQL database
* CRUD operations
* Row Level Security
* User-owned data protection

### Phase 3: AWS Integrations

Selected AWS services will be added where they provide clear value for:

* Automation
* Monitoring
* Storage
* Email notifications
* AI-assisted workflows

### Phase 4: Portfolio-Ready Release

* Automated testing
* Architecture diagrams
* Database ERD
* Security documentation
* Accessibility review
* Demo video
* Project case study
* Deployment documentation

## Cloud Cost Strategy

Career HQ will be developed with a maximum target budget of **$40 per month**.

### Budget Goals

| Stage                       | Target Monthly Cost |
| --------------------------- | ------------------: |
| Frontend MVP                |                  $0 |
| Supabase full-stack version |              $0–$25 |
| AWS integrations            |              $0–$15 |
| Maximum development budget  |                 $40 |

The project will prioritize:

* Free-tier services
* Student benefits and credits
* Serverless technologies
* Pay-for-use services
* Monthly cost monitoring
* Incremental service adoption
* Documented architecture decisions

No paid service will be added unless it provides clear value to the application or portfolio.

## Security Goals

Career HQ will store private career and employment information. Security is a core requirement.

Planned security practices include:

* Secure authentication
* Row Level Security on user-owned database tables
* Least-privilege access
* Input validation
* Secure credential management
* No service-role keys exposed in the browser
* Protected document access
* Audit and activity logging
* Secure error handling
* Regular dependency reviews

## Accessibility Goals

Career HQ will be designed to support a wide range of users.

Accessibility goals include:

* Semantic HTML
* Keyboard navigation
* Visible focus states
* Clear form labels
* Readable color contrast
* Plain-language instructions
* Mobile-friendly touch targets
* Clear validation and error messages
* No reliance on color alone
* WCAG 2.2 AA as a long-term target

## ADHD-Friendly Design Principles

Career HQ is designed to reduce overwhelm through:

* One clear next action
* A maximum of three daily priorities
* Visual progress indicators
* Smaller, manageable tasks
* Consistent page layouts
* Quick-capture tools
* Reminder dates
* Plain-language instructions
* Minimal unnecessary distractions

## Project Structure

```text
career-hq/
├── README.md
├── CHANGELOG.md
├── LICENSE
├── index.html
├── css/
│   └── style.css
├── js/
│   └── app.js
├── assets/
│   ├── images/
│   └── icons/
├── database/
│   ├── schema.sql
│   └── policies.sql
├── docs/
│   ├── product-requirements.md
│   ├── system-design.md
│   ├── architecture-decisions.md
│   ├── database-design.md
│   ├── security.md
│   ├── accessibility.md
│   ├── testing.md
│   ├── cloud-costs.md
│   └── deployment.md
├── screenshots/
├── tests/
└── demo/
```

The directory structure may change as the application develops.

## Development Roadmap

### Version 1: Project Foundation

* Create repository structure
* Add project documentation
* Build the landing page
* Create dashboard wireframes
* Define the initial data model

### Version 2: Frontend Prototype

* Build responsive navigation
* Create dashboard components
* Add sample job applications
* Add local form validation
* Test mobile layouts

### Version 3: Supabase Integration

* Add user authentication
* Create PostgreSQL tables
* Implement CRUD operations
* Add Row Level Security
* Test user data isolation

### Version 4: Career Management Tools

* Add Resume HQ
* Add Interview HQ
* Add Salary Research
* Add email templates
* Add application-document management

### Version 5: AWS Integration

* Add S3 backups or storage
* Add Lambda automation
* Add EventBridge reminders
* Add SES notifications
* Add CloudWatch monitoring

### Version 6: AI Assistance

* Add AI interview preparation
* Add resume-to-job analysis
* Add career task suggestions
* Add follow-up drafting
* Add Amazon Bedrock or another approved AI service

### Version 7: Portfolio Release

* Complete testing
* Improve accessibility
* Add architecture diagrams
* Add database ERD
* Record demo video
* Publish case study
* Create a tagged GitHub release

## Current Project Status

Career HQ is currently in the **planning and early development stage**.

Current work includes:

* Defining product requirements
* Designing the application workflow
* Planning the database
* Documenting security requirements
* Creating the cloud cost strategy
* Planning Supabase and AWS integration
* Preparing the initial user interface

Features listed in this README are marked as planned until they are implemented and tested.

## Development Roadmap

Career HQ is being developed incrementally, with each version focused on a clear product milestone.

- ✅ **v0.2.0 — Professional Landing Page**
- 🚧 **v0.3.0 — Design System and Dashboard UI**
- ⬜ **v0.4.0 — Authentication**
- ⬜ **v0.5.0 — Job Applications**
- ⬜ **v0.6.0 — Resume HQ**
- ⬜ **v0.7.0 — Interview HQ**
- ⬜ **v0.8.0 — Certifications**
- ⬜ **v0.9.0 — AI Assistant**
- ⬜ **v1.0.0 — Production Release**

For detailed goals and planned features, see the [full development roadmap](docs/ROADMAP.md).

## Project Documentation

Detailed project documentation is available in the [`docs`](docs/) directory.

- [Product Requirements](docs/PRODUCT_REQUIREMENTS.md)
- [System Architecture](docs/SYSTEM_ARCHITECTURE.md)
- [Database Design](docs/DATABASE_DESIGN.md)
- [Security](docs/SECURITY.md)
- [UI/UX Guidelines](docs/UI_UX_GUIDELINES.md)
- [Development Roadmap](docs/ROADMAP.md)
- [Contributing Guide](docs/CONTRIBUTING.md)

## Skills Demonstrated

This project is designed to demonstrate:

* Product planning
* Full-stack development
* Responsive web design
* JavaScript
* PostgreSQL
* Supabase
* Authentication and authorization
* Row Level Security
* AWS cloud architecture
* Serverless computing
* Cloud cost optimization
* Git and GitHub
* CI/CD
* Security planning
* Accessibility
* Testing
* Documentation
* AI integration
* DevOps practices

## Architecture Decisions

Major technical decisions will be documented in Architecture Decision Records.

Initial decisions include:

* Use Supabase for the MVP to reduce development complexity
* Use PostgreSQL because Career HQ contains relational data
* Use GitHub Pages for free frontend hosting
* Add AWS services selectively instead of migrating everything immediately
* Keep development costs at or below $40 per month
* Build the core application before introducing AI features

## Screenshots

Screenshots and interface previews will be added as development progresses.

## Documentation

Planned documentation includes:

* Product Requirements Document
* System Design
* Database Design
* Architecture Decision Records
* Security Plan
* Accessibility Plan
* Testing Plan
* Cloud Cost Estimates
* AWS Integration Strategy
* Deployment Guide
* Portfolio Case Study

## Author

**Chassidy Barker**

Cloud Computing student focused on cloud architecture, AI, DevOps, automation, and secure application development.

* GitHub: [chassbarker](https://github.com/chassbarker)
* LinkedIn: [Chassidy Barker](https://www.linkedin.com/in/chassidy-barker-02478535a)
* Portfolio: [chassidybarker.com](https://chassidybarker.com)

## License

This project is licensed under the MIT License.
