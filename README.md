# Issue Tracking System

A full-stack issue management application built with **Java, Spring Boot, React.js, and MongoDB** to streamline technical issue reporting, tracking, prioritization, and resolution through a structured workflow.

The system provides role-based access, issue lifecycle management, activity tracking, and administrative monitoring to support efficient troubleshooting and reliable issue resolution.

## 🚀 Key Features

- **Issue Lifecycle Management:** Create, view, edit, delete, search, and filter issues.
- **Authentication & Authorization:** User registration, login, BCrypt password hashing, and role-based access control.
- **Issue Prioritization:** Track issue type, priority, status, assignee, and due date.
- **Workflow Management:** Manage issues through Open, In Progress, Resolved, and Closed statuses.
- **Role-Based Permissions:** Users manage their own issues, while administrators can oversee issues across users.
- **Technical Issue Categorization:** Twelve issue categories with automatic recommended-team assignment.
- **Activity Tracking:** Maintain comments, activity history, and status-change information.
- **Administrative Dashboard:** View issue summaries, open issues, completed issues, and high-priority issues.
- **Notifications:** Provide users with notifications and identify administrator-initiated status changes.
- **Responsive Interface:** Access issue management features through a responsive React frontend.
- **API Validation & Error Handling:** Validate requests and provide user-friendly error responses.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Java 17 | Backend programming |
| Spring Boot | REST API development and backend services |
| Spring Security / BCrypt | Authentication-related security and password hashing, where configured |
| React.js | Frontend development |
| MongoDB | Persistent data storage |
| Maven | Backend dependency and build management |
| Node.js & npm | Frontend tooling and dependency management |
| Swagger UI / OpenAPI | API documentation |
| Git & GitHub | Version control and source code management |

## 🏗️ Architecture

The application follows a frontend-backend architecture:

1. **React Frontend:** Provides the user interface for authentication, issue management, dashboards, and activity tracking.
2. **Spring Boot Backend:** Processes requests, applies business rules, validates input, and exposes REST APIs.
3. **MongoDB Database:** Stores application data, including issues and related records.

```text
                 User
                  |
                  v
          React.js Frontend
          localhost:3000
                  |
              REST APIs
                  |
                  v
          Spring Boot Backend
          localhost:8080
                  |
                  v
              MongoDB
          localhost:27017
```

## 🔄 Issue Workflow

Issues progress through the following statuses:

`Open → In Progress → Resolved → Closed`

The available transitions depend on the user's role and the configured workflow permissions.

## 🔐 Role-Based Access

### User
- Register and log in securely.
- Create and manage personally owned issues.
- Search, filter, and track issue status.
- Add comments and review activity history.

### Administrator
- Access the administrative dashboard.
- View and manage issues across users.
- Review issue summaries and priority levels.
- Perform additional workflow transitions permitted by the application.

## ⚙️ Installation & Setup

### Prerequisites

Install the following before running the application:

- Java Development Kit (JDK) 17
- Apache Maven
- Node.js 18 or later
- MongoDB running locally or an accessible MongoDB instance
- Git

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_PROJECT_DIRECTORY>
```

Replace the placeholders with your actual repository URL and directory name.

### 2. Start the MongoDB Database

Ensure MongoDB is running and accessible at:

```text
mongodb://localhost:27017
```

Configure the database name and connection settings according to your backend configuration.

### 3. Run the Spring Boot Backend

Open a terminal and navigate to the backend directory:

```bash
cd backend
mvn clean package
mvn spring-boot:run
```

The backend is expected to run at:

```text
http://localhost:8080
```

### 4. Run the React Frontend

Open another terminal from the project root:

```bash
cd frontend
npm install
npm start
```

The frontend is expected to run at:

```text
http://localhost:3000
```

## 📚 API Documentation

When the backend is running, access Swagger UI at:

http://localhost:8080/swagger-ui/index.html

The main issue API endpoint is:

```text
http://localhost:8080/api/issues
```

Available operations depend on the backend's implemented endpoints and access permissions.

## 🔒 Security Configuration

For development, the application supports an automatically configured administrator account.

For environments outside development:

- Set `ADMIN_NAME`, `ADMIN_EMAIL`, and `ADMIN_PASSWORD` through environment variables.
- Set `ADMIN_REGISTRATION_CODE` to a private value.
- Never commit real credentials, secrets, or private configuration values to GitHub.
- Replace any default development credentials before deploying the application.

The development credentials and registration code should only be used in a controlled local environment. If these values have already been published in a public repository, rotate them and review the application's configuration.

## 💡 Skills Demonstrated

This project demonstrates practical skills relevant to software engineering and technical support roles:

- **Java Development:** Object-oriented programming and backend application development.
- **Technical Troubleshooting:** Issue reporting, categorization, prioritization, and resolution tracking.
- **REST API Development:** Communication between frontend and backend services.
- **Database Management:** Persistent storage and data retrieval using MongoDB.
- **Testing & Debugging:** API validation, error handling, and application verification.
- **System Reliability:** Structured workflows and centralized issue tracking.
- **Access Control:** Role-based permissions and authentication-related security.
- **Technical Documentation:** Setup instructions, API documentation, and project documentation.
- **Software Maintenance:** Organized issue records and activity history to support ongoing maintenance.
- **Problem-Solving & Collaboration:** A structured approach to tracking technical issues and coordinating their resolution.

## 🎯 Project Objective

To develop a centralized issue management system that helps users report technical problems, track their progress, prioritize critical issues, and support administrators in managing issue resolution efficiently.

## 🔮 Future Enhancements

- Automated email notifications for issue assignments and status changes.
- Advanced analytics and issue-resolution reports.
- Automated testing and continuous integration with GitHub Actions.
- Deployment using a cloud hosting platform.
- Integration with monitoring tools for automated incident creation.


Replace the profile links above with your actual URLs before publishing.

---

*Built with Java, Spring Boot, React.js, and MongoDB.*
