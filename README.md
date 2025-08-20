# airbnb-clone-project

## Project Overview

The projects seeks to provide a comprehensive, real-world application designated to simulate the development of booking platform like Airbnb. It involves a dive into the backend systems, database design, API developmemnt, security and best practices. This project aims to enable a deep understanding of complex architectures, workflows, and collaborative team dynamics geared towards building a scalable web application.

## Technology Stack

Technology stack to be used in this project are as follows:

- Django: A Python web framework used for building the RESTful API.
- PostgreSQL: A powerful relational database (RDBM) used for data storage.
- GraphQL: Allows for flexible and efficient querying of data.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes, and also aids seamless of apps from development to production.

## Team Roles

- Business Analyst: This individual is responsible in understanding customer's business processes, translating customer business needs into requirements.
- Product owner (PO): Responsible for product vision and evolution, making sure the final product meets customer requirements.
- Project Manager (PM): Ensures product on-time delivery, and within budget. Spearheads software development team.
- UI/UX Designer (UX): Transform a product vision into user-friendly interface. Creates user journey for the best user experience.
- Software Architect (SA): Designs a high-level software architecture, selecting appropriate tools and technologies to implement the product vision.
- Software developer: Engineers and stabilizes the product, solves any technical problems emerging during the development process.
- Quality Assurance (QA) engineer: Ensures an application performs according to requirements, spots functional and non-functional defects.
- DevOps engineer: Facilitates cooperation between development and operations teams.
- Test Automation Engineer (TA): Designs a test automation ecosystem.

## Database Design

Key entities (Users, Properties, Bookings, Reviews, and Payments)

| Entity   | Fields   | Relationship                                                                       |
|----------|----------|------------------------------------------------------------------------------------|
| User     | Name, Age, Occupation    | 1 to Many mapping to (Properties, Bookings, Reviews, Payments)     |
| Properties    | Location, Type, Class   | 1 to 1 mapping to (Users, Bookings, Payments, reviews)         |
| Bookings | Date, Duration, CustomerName | 1 to 1 mapping to (Users, Payments) |
| Reviews | Date, Comments, Rating | 1 to 1 mapping to (Users, Properties) |
| Payments | Date, Amount, Property | 1 to 1 mapping to (Users, Properties, Bookings) |

Anology on sample fields to be included in the database.

## Feature Breakdown

- User management: This ensures proper registration, authentication, and profile management.
- Property management: Enables property listing operations like creation, update, and retrieval.
- Booking system: Enables booking management, comprising of check-in and check-out details of properties.
- Payment system: Handles payment transactions related to bookings.
- Review system: Helps with the management of reviews for properties.
- System Documentation: Provides a well-documented system design process for subsequent improvement and integration to other platforms.

## API Security Overview

A key backend responsibility is ensuring seamless communication between different application components (such as user interfaces and databases) through a technology called APIs. However, a security leak in the API could result in serious consequences, exposing personal user data (leading to privacy issues) or allowing attackers to hijack business processes and even financial transactions.

To mitigate these risks, several security measures must be implemented, such as:

- Authentication: Implementing a robust authentication mechanisms (e.g JWT tokens, session-based cookies, OAuth), or enforcing strong password policies, and ensuring secure multi-factor authentication (MFA) for users, helps to ensure only legitimate users and services can access the API.

- Authorization: While role-based access control (RBAC) or attribute-based access control (ABAC), can be set in place in enfore least-privilege principles, where users/services can only access what they need. This helps reduces damage radius when account is compromised.

- Rate limiting: Added with throttling, this ensures gaps in api requests, reducing tendencies of overloading the api server. It also ensures a fair usage policies for legitimate users.

## CI/CD Pipeline Overview

CI/CD (Continuous Integration and Continuous Deployment) is a critical practice in the software delivery lifecycle, bridging the gap between development and production. It automates key stages such as building, testing, vulnerability scanning, and deployment, ensuring that code changes are delivered quickly, reliably, and securely.

They reduce errors due to human, speed up delivery, enhance code quality, and provide early detection of bugs or vulnerabilities. This ensures that the project remains stable, secure, and scalable as new features are introduced. Tools commonly used in CI/CD include, GitHub Actions, GitLab CI/CD, Jenkins, and CircleCI for pipeline automation, combined with Docker and Kubernetes for containerization and orchestration.
