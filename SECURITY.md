# Security Policy

This document outlines the key security principles implemented in the IT Ticketing System, with considerations for secure authentication, data handling, and role-based access.

---

#  Overview

The IT Ticketing System prioritizes user safety and system integrity through:

- Secure user authentication and password management
- Input validation and protection against injection attacks
- Role-based authorization and route control
- Activity logging for auditability and incident response

---

#  Authentication & Authorization

- Passwords are securely hashed using `werkzeug.security` before being stored in the database.
- User roles include `admin`, `technician`, and `user`, each with scoped access.
- Flask-Login manages session-based authentication and protects endpoints using `@login_required`.

---

#  Input Validation & Threat Mitigation

- All form inputs are sanitized to defend against SQL injection and XSS attacks.
- Content validation is implemented at both frontend (client-side constraints) and backend (server-side checks).
- Planned extensions include additional threat detection via regex filtering and field whitelisting.

---

# Logging & Monitoring

- Key user actions (e.g. ticket updates, login attempts) are logged with timestamps and user IDs.
- Logs can be extended for integration with SIEM tools or alerting systems like Slack or email.
- Future iterations may incorporate anomaly detection and multi-factor authentication (MFA).

---

# Best Practices Followed

| Practice                   | Status       |
|----------------------------|--------------|
| Hashed Password Storage     | ✅ Implemented |
| Role-Based Access Control   | ✅ Implemented |
| Input Validation            | ✅ In Progress |
| Logging & Auditing          | ✅ Partial     |
| HTTPS Encryption            | 🔜 Future work |
| MFA                        | 🔜 Future work |
| Dependency Audit           | 🔜 Planned     |

---

# Future Security Enhancements

- Enforce HTTPS across all endpoints using Flask-Talisman or a reverse proxy
- Implement MFA for admins and technicians
- Create an audit log viewer for admins to trace system changes
- Add rate limiting and CAPTCHA for login form to reduce brute-force attempts

---

# Reporting Vulnerabilities

If you discover a vulnerability in this project, please open an issue with the label `security` or contact me directly via [LinkedIn). Responsible disclosure is appreciated.

