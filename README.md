# Victorious School Pro

A commercial-ready **development/MVP foundation** for school fee and family management. It is a Java 17 Maven Swing application with SQLite.

## Included
- Login and role-based access: ADMIN, FINANCE, STAFF
- PBKDF2-HMAC-SHA256 password hashing
- Family management and family codes
- Grade R-12 student records
- Annual fee totals and family statements
- Bank CSV import and automatic family-code matching
- Duplicate-safe transaction references
- January-June and July-December PDF letters
- User administration
- Database backup
- Audit log
- SQLite WAL mode and foreign-key enforcement
- Dashboard

## First run
1. Open the folder in NetBeans as a Maven project.
2. Use JDK 17+.
3. Run `za.victoriousschool.Main`.
4. The first run automatically creates the database and administrator account.

Default development login:
- Username: `admin`
- Password: `Admin@123`

Change the default password before any real deployment.

## Bank CSV
The included test CSV uses:
`date,description,reference,amount`

The `reference` must match an existing family code, e.g. `FAM1001`.

## Commercial deployment checklist
This project is a solid application foundation, but no software should be sold as production-ready solely from source code without QA, security review, backups/restore testing, legal/privacy review, deployment monitoring, and school-specific requirements. Before commercial launch add:
- HTTPS and a hosted multi-school backend if remote access is required
- Per-school tenancy and subscription/licensing
- Password reset/MFA and account lockout
- Fine-grained permissions and server-side authorization
- Bank-specific statement adapters and reconciliation approval workflow
- Fee schedules per term/month, discounts, bursaries, arrears and credits
- Receipt numbering and accounting exports
- Full reporting and audit review UI
- Automated backups and disaster recovery
- POPIA/privacy controls, retention policies and data export/deletion procedures
- Automated tests, penetration testing, dependency updates and signed releases
- School onboarding/settings, branding and support tools
