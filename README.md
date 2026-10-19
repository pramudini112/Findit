# FindIt — University Lost & Found Management System

A web-based platform that helps university students report, search for, and recover lost belongings through a centralized lost and found system.

## About the Project

Students frequently lose personal belongings such as identity cards, keys, water bottles, wallets, and headphones around university premises. Finding these belongings can be difficult when information is scattered across social media, notice boards, and informal communication channels.

**FindIt** aims to simplify this process by providing a centralized platform where students can report lost or found items, search existing reports, and discover potential matches using rule-based matching.

The project focuses on making lost-item recovery more organized, accessible, and secure within a university environment.

## Objectives

- Provide a centralized platform for lost and found reports.
- Allow students to submit and manage lost and found item reports.
- Enable searching and filtering by keywords, category, location, and report type.
- Suggest potential matches between lost and found items.
- Provide safe contact instructions or claim requests for recovering belongings.
- Enable administrators to moderate inappropriate or suspicious reports.
- Support item status updates when belongings have been recovered.

## Key Features

### User Management
- User registration and login.
- Secure authentication and access control.
- Personal dashboard for managing submitted reports.

### Lost & Found Reporting
- Submit lost-item and found-item reports.
- Include item descriptions, categories, dates, and locations.
- Optionally upload item images.
- View detailed information about reported items.

### Search & Filtering
- Search items using keywords.
- Filter by lost or found status.
- Filter by item category and location.
- Browse recently reported items.

### Rule-Based Matching
- Compare lost and found reports using item categories, description keywords, locations, and dates.
- Suggest potentially matching reports.
- Help users identify relevant reports without relying on advanced AI or machine learning.

### Claim & Recovery
- Provide safe contact instructions or a basic claim request process.
- Allow users to update report status.
- Mark reports as resolved once belongings have been recovered.

### Administrative Moderation
- Review submitted reports.
- Remove or disable inappropriate or suspicious content.
- Restrict administrative functions to authorized administrators.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | React |
| Frontend Styling | CSS / Bootstrap |
| Backend | Java Spring Boot |
| API | REST API |
| Database | PostgreSQL |
| Authentication & Security | Spring Security |
| Version Control | Git and GitHub |
| Testing | JUnit and frontend/API testing tools |

*The technology stack is the planned implementation stack and may be updated as development progresses.*

## System Architecture

FindIt follows a client-server architecture.

1. **Frontend:** React provides the user interface for reporting, browsing, searching, and managing items.
2. **Backend:** Spring Boot provides REST APIs, validates requests, applies business rules, manages permissions, and performs matching.
3. **Database:** PostgreSQL stores user accounts, item reports, report statuses, and related information.
4. **Matching component:** Rule-based logic compares eligible lost and found reports and returns possible matches.

```text
             User
              |
              v
       React Frontend
              |
          REST API
              |
              v
      Spring Boot Backend
         /           \
        v             v
  PostgreSQL      Matching Logic
        |
        v
 Users, Items,
 Claims & Statuses
```

## User Roles

**Guest User**
- Browse available reports.
- Search and filter items.
- View permitted item details.

**Registered User**
- Submit lost and found reports.
- Manage personal reports.
- View possible matches.
- Submit claim requests or follow contact instructions.
- Update report status.

**Administrator**
- Review reports.
- Remove or disable inappropriate content.
- Perform authorized moderation tasks.

## Project Structure

The repository is organized as a single project containing the frontend and backend.

```text
findit-lost-and-found/
├── frontend/          # React application
├── backend/           # Spring Boot application
├── database/          # Database scripts and setup
├── docs/              # Project documentation and diagrams
├── README.md
└── .gitignore
```

*Directories will be added as development progresses.*

## Getting Started

### Prerequisites

Install the following tools before running the application:

- [Node.js and npm](https://nodejs.org/)
- [Java JDK](https://adoptium.net/)
- [Git](https://git-scm.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Visual Studio Code](https://code.visualstudio.com/) or another suitable IDE

A compatible Java version will be selected when configuring the Spring Boot project.

### Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
cd findit-lost-and-found
```

Replace `YOUR_REPOSITORY_URL` with the repository URL from GitHub.

### Run the Application

**Frontend**

After the React application has been created:

```bash
cd frontend
npm install
npm run dev
```

**Backend**

After the Spring Boot application has been created and its database configuration is complete, run it using the Maven wrapper generated with the project:

Windows:

```powershell
cd backend
.\mvnw.cmd spring-boot:run
```

macOS / Linux:

```bash
cd backend
./mvnw spring-boot:run
```

The application cannot run fully until the required project files, dependencies, and database configuration have been created.

## Security & Privacy

FindIt aims to protect users and their information by:

- Storing passwords using secure password hashing.
- Restricting report management to authorized users.
- Protecting administrator functions through access control.
- Avoiding public exposure of private contact details.
- Avoiding the public display of sensitive information on identity documents.
- Treating matching results as suggestions rather than proof of ownership.

## Project Scope

The initial release focuses on essential lost and found functionality and simple rule-based matching.

**Included**
- Authentication and user management.
- Lost and found reporting.
- Search and filtering.
- Item details and report management.
- Rule-based matching suggestions.
- Basic claim/contact functionality.
- Item status management.
- Administrative moderation.

**Planned for future versions**
- Advanced AI-powered matching.
- Real-time in-app messaging.
- Email or push notifications.
- Advanced analytics.
- Mobile applications.

## Development Workflow

The project is developed collaboratively using Git and GitHub.

- Work on separate branches for new features.
- Use descriptive commit messages.
- Test changes before merging.
- Review and integrate contributions through pull requests when practical.
- Keep documentation updated as the system evolves.
- Never commit passwords, API keys, database credentials, or other secrets.

## Testing

Testing will cover:

- Registration and authentication.
- Lost and found report submission.
- Search and filtering.
- Report ownership and authorization.
- Rule-based matching scenarios.
- Claim/contact workflows.
- Status updates.
- Administrative moderation.
- Input validation and error handling.

## Project Documentation

Supporting documentation and diagrams will be maintained in the `docs/` directory as they become available.

## Team

**Project:** FindIt — University Lost & Found Management System

**Team Members:**
- Team Member 1: *Add name*
- Team Member 2: *Add name*

## Project Status

**Status:** Initial development and setup.

FindIt is being developed as a university software development project. Features described in this README represent the planned scope and should not be considered implemented until they have been developed and tested.

## License

No license has been selected yet. The project is currently intended for academic development. A license may be added after the team agrees on the intended distribution and reuse terms.

