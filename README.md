# IT Ticketing System

An intuitive, role-based ticketing application built using Python and Flask. Designed to streamline internal IT support with secure authentication, dashboard metrics, and user-friendly ticket management.

---

 Features

- Submit and track support tickets
- Role-based authentication: Admin, Technician, and User
- Metrics dashboard: Ticket statistics and progress tracking
- Security features: hashed passwords, input validation, and activity logging
- Built with Flask, SQLite, and Bootstrap

---

Motivation

This project was built as part of my cybersecurity studies and reflects my interest in secure and scalable system design. It’s also intended to demonstrate hands-on development, practical security principles, and GitHub-friendly organization.

---

Tech Stack

| Layer        | Tools                            |
|--------------|----------------------------------|
| Backend      | Flask, Python                    |
| Frontend     | HTML, CSS (Bootstrap), JavaScript |
| Database     | SQLite + SQLAlchemy              |
| Auth         | Flask-Login, Werkzeug            |
| Security     | Hashed credentials, logging, validation |

---

Security Highlights

- Passwords are hashed using `werkzeug.security`
- User input sanitized to prevent SQL injection and XSS
- Routes protected with `@login_required` and role checks
- Admin dashboard logs key user actions for traceability

