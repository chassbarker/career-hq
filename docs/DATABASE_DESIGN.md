# Career HQ Database Design

| Property | Value |
| --- | --- |
| Document | Database Design |
| Project | Career HQ |
| Document Version | 0.2.0 |
| Product Version | 0.2.0 |
| Status | In Development |
| Author | Chassidy Barker |
| Last Updated | July 2026 |

---
`n## Overview

Career HQ will use PostgreSQL through Supabase to store user-owned career data securely.

The database is designed to support:

- User profiles
- Job applications
- Resume versions
- Interviews
- Salary research
- Projects
- Certifications
- Tasks
- Networking contacts
- Weekly accomplishments
- Notes and ideas

The design will follow relational database best practices, including:

- Primary keys
- Foreign keys
- Data validation
- Indexes
- Row Level Security
- User ownership
- Least-privilege access

---

## Design Principles

### User-Owned Data

Most records will belong to one authenticated user.

Each user-owned table will include:

```text
user_id
```

This value will reference the authenticated user's profile and will be protected using Row Level Security.

### UUID Primary Keys

Primary keys will use UUID values instead of sequential integers.

Example:

```sql
id uuid primary key default gen_random_uuid()
```

### Timestamps

Most tables will include:

```text
created_at
updated_at
```

These fields will help track when records are created or changed.

### Data Integrity

The database will use:

- `NOT NULL` constraints
- Foreign keys
- Check constraints
- Unique constraints
- Default values
- Appropriate data types

---

## Core Tables

## 1. profiles

### Purpose

Stores user profile information and application preferences.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key and authenticated user ID |
| full_name | text | User's display name |
| email | text | User email address |
| preferred_role | text | Main career target |
| location | text | User location |
| timezone | text | User timezone |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Relationships

- One profile can own many applications.
- One profile can own many resumes.
- One profile can own many interviews.
- One profile can own many tasks.
- One profile can own many projects.
- One profile can own many certifications.

### Security

Users may only view and update their own profile.

---

## 2. applications

### Purpose

Stores job application records from discovery through final outcome.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Owner of the application |
| company_name | text | Employer name |
| position_title | text | Job title |
| location | text | Job location |
| work_arrangement | text | Remote, hybrid, or on-site |
| employment_type | text | Full-time, part-time, contract, or internship |
| posting_url | text | Original job posting |
| date_found | date | Date the job was discovered |
| application_deadline | date | Application deadline |
| date_applied | date | Date submitted |
| status | text | Current application status |
| recruiter_name | text | Recruiter or contact name |
| recruiter_email | text | Recruiter or contact email |
| next_action | text | Next required step |
| next_action_date | date | Due date for next action |
| outcome | text | Final result |
| notes | text | Additional notes |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Suggested Status Values

```text
Saved
Researching
Preparing
Applied
Interviewing
Offer
Rejected
Withdrawn
Closed
```

### Relationships

- One application can have many documents.
- One application can have many interviews.
- One application can have one or more salary research records.
- One application may reference one submitted resume.

### Indexes

Recommended indexes:

```text
user_id
status
next_action_date
date_applied
company_name
```

### Security

Users may only create, view, edit, and delete their own applications.

---

## 3. resumes

### Purpose

Stores resume versions and related metadata.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Owner of the resume |
| name | text | Resume name |
| target_role | text | Intended role |
| version | text | Version label |
| file_path | text | Secure storage path |
| is_master | boolean | Indicates master resume |
| notes | text | Revision notes |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Example Resume Names

```text
Master Resume
Cloud Engineer Resume
DevOps Resume
AI Resume
Web Developer Resume
Submitted Resume
```

### Relationships

- One resume can be linked to many applications.
- One application can reference the exact resume submitted.

### Security

Resume documents must be stored privately. Users may only access their own files and metadata.

---

## 4. application_documents

### Purpose

Stores documents associated with job applications.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| application_id | uuid | Related application |
| document_type | text | Resume, cover letter, job description, or other |
| file_name | text | Original file name |
| file_path | text | Secure storage location |
| notes | text | Optional notes |
| created_at | timestamptz | Record creation date |

### Suggested Document Types

```text
Resume
Cover Letter
Job Description
Application Answers
Interview Preparation
Thank-You Email
Follow-Up Email
Offer
Rejection
Other
```

### Security

Users may only access documents connected to their own applications.

---

## 5. interviews

### Purpose

Stores interview schedules, preparation, notes, and reflections.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| application_id | uuid | Related job application |
| interview_type | text | Phone, video, technical, panel, or final |
| interview_date | timestamptz | Scheduled date and time |
| interviewer_names | text | Interviewer names and roles |
| location_or_link | text | Meeting location or URL |
| preparation_notes | text | Research and preparation |
| questions_asked | text | Questions asked during interview |
| strong_answers | text | Answers that went well |
| improvement_notes | text | Areas to improve |
| next_steps | text | Expected next steps |
| thank_you_sent | boolean | Whether thank-you email was sent |
| follow_up_date | date | Follow-up reminder |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Relationships

- Many interviews can belong to one application.

### Indexes

Recommended indexes:

```text
user_id
application_id
interview_date
follow_up_date
```

---

## 6. salary_research

### Purpose

Stores compensation research for a job opportunity.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| application_id | uuid | Related application |
| salary_listed | boolean | Whether the posting listed compensation |
| listed_min | numeric | Listed minimum salary |
| listed_max | numeric | Listed maximum salary |
| market_min | numeric | Estimated market minimum |
| market_max | numeric | Estimated market maximum |
| target_min | numeric | User target minimum |
| target_max | numeric | User target maximum |
| private_minimum | numeric | Private minimum acceptable salary |
| hourly_equivalent | numeric | Hourly equivalent |
| sources | text | Sources checked |
| location_adjustment | text | Cost-of-living notes |
| research_date | date | Research date |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Relationships

- Salary research belongs to one application.
- One application may have multiple research updates over time.

### Security

Salary expectations and private minimums must remain visible only to the record owner.

---

## 7. projects

### Purpose

Stores portfolio, school, cloud, AI, and development projects.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| title | text | Project name |
| project_type | text | Portfolio, school, cloud, AI, or other |
| description | text | Project summary |
| status | text | Planning, active, paused, or completed |
| repository_url | text | GitHub repository |
| live_url | text | Live demonstration |
| technologies | text[] | Technologies used |
| lessons_learned | text | Key lessons |
| portfolio_summary | text | Portfolio-ready description |
| start_date | date | Project start date |
| completion_date | date | Completion date |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Suggested Status Values

```text
Idea
Planning
In Progress
Testing
Completed
Paused
Archived
```

---

## 8. certifications

### Purpose

Stores certifications, badges, and credentials.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| name | text | Certification or badge name |
| issuing_organization | text | Issuer |
| issue_date | date | Date earned |
| expiration_date | date | Expiration date |
| credential_id | text | Credential identifier |
| credential_url | text | Verification or Credly link |
| badge_image_url | text | Badge image |
| skills | text[] | Skills demonstrated |
| notes | text | Additional details |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Indexes

Recommended indexes:

```text
user_id
issue_date
expiration_date
issuing_organization
```

---

## 9. tasks

### Purpose

Stores priorities, reminders, deadlines, and next actions.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| title | text | Task name |
| description | text | Task details |
| category | text | Application, interview, project, school, or other |
| priority | text | Low, medium, or high |
| status | text | To do, in progress, or completed |
| due_date | timestamptz | Task due date |
| related_record_type | text | Related entity type |
| related_record_id | uuid | Related record |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

### Suggested Categories

```text
Application
Interview
Resume
Project
Certification
School
Networking
General
```

---

## 10. contacts

### Purpose

Stores recruiters, interviewers, mentors, and networking contacts.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| full_name | text | Contact name |
| company | text | Company or organization |
| job_title | text | Contact role |
| email | text | Email address |
| phone | text | Phone number |
| linkedin_url | text | LinkedIn profile |
| relationship_type | text | Recruiter, mentor, interviewer, or networking contact |
| last_contact_date | date | Most recent contact |
| next_follow_up_date | date | Follow-up reminder |
| notes | text | Conversation notes |
| created_at | timestamptz | Record creation date |
| updated_at | timestamptz | Last update date |

---

## 11. weekly_wins

### Purpose

Stores achievements, completed work, and lessons learned.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| week_start | date | Start of the week |
| accomplishment | text | Achievement or completed task |
| lesson_learned | text | Lesson or reflection |
| portfolio_ready | boolean | Whether it can be used in portfolio content |
| linkedin_ready | boolean | Whether it can be used in a LinkedIn post |
| created_at | timestamptz | Record creation date |

---

## 12. brain_dump

### Purpose

Stores unsorted ideas, reminders, and notes for later organization.

### Planned Columns

| Column | Type | Description |
| --- | --- | --- |
| id | uuid | Primary key |
| user_id | uuid | Record owner |
| content | text | Captured thought or idea |
| processed | boolean | Whether it has been organized |
| created_at | timestamptz | Record creation date |
| processed_at | timestamptz | Date processed |

---

## Relationships Summary

```text
profiles
│
├── applications
│   ├── application_documents
│   ├── interviews
│   └── salary_research
│
├── resumes
├── projects
├── certifications
├── tasks
├── contacts
├── weekly_wins
└── brain_dump
```

---

## Row Level Security

Row Level Security will be enabled on every user-owned table.

The expected ownership rule is:

```sql
auth.uid() = user_id
```

Users should only be able to:

- View their own records
- Create records assigned to their own user ID
- Update their own records
- Delete their own records

Service-role credentials must never be exposed in browser code.

---

## Storage Design

Supabase Storage may be used for:

- Resume files
- Cover letters
- Job descriptions
- Certification evidence
- Screenshots
- Portfolio documents

Storage buckets should be private by default.

Suggested folder structure:

```text
user-id/
├── resumes/
├── applications/
├── certifications/
└── projects/
```

---

## Validation Rules

Examples of planned validation:

- Required text fields must not be blank.
- Email fields must contain valid email formats.
- URLs must use valid URL formats.
- Salary values must be zero or greater.
- End dates must not occur before start dates.
- Status values must match approved options.
- Users may not assign records to another user ID.

---

## Indexing Strategy

Indexes will be added to columns commonly used for:

- Filtering
- Sorting
- Searching
- Foreign-key relationships
- Upcoming dates
- Application status

Indexes should be added based on actual query patterns rather than preemptively indexing every column.

---

## Backup and Recovery

Planned protections include:

- Supabase database backups
- Exported schema files
- Version-controlled migrations
- Periodic data exports
- Documented restoration procedures

---

## Future Database Enhancements

Possible future additions include:

- Audit logs
- Notifications
- Email templates
- AI-generated recommendations
- Saved job searches
- Application analytics
- Dashboard preferences
- Multi-user or team support
- Role-based permissions

---

## Current Status

The database is currently in the planning stage.

This document defines the initial relational design and will be updated as:

- Supabase is configured
- Tables are created
- Relationships are tested
- Row Level Security policies are implemented
- Application requirements change
