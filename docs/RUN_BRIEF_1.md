# Run Brief: CampusConnect UNT

## Problem and user
UNT students cannot easily find and register for events run by Registered Student Organizations (RSOs). Build a small responsive web app where students browse and register for events, and RSO leaders publish events, see registrations, and record attendance. Users: students (phone or laptop) and RSO leaders.

## Must-dos (each testable)
1. Users create an account (unique email, password of 8+ characters), log in, and log out. Logged-out users cannot open protected pages.
2. Two roles: student and leader. A new "leader" sign-up is pending and has no leader privileges until an admin or the seed script approves it and links it to an RSO. Leader pages return 403 to students, pending leaders, and leaders of other RSOs.
3. Approved leaders create events: title, description, date, time, campus location, capacity of at least 1. Invalid input shows a clear error.
4. Logged-in users see upcoming events (not past) and search by event title or RSO name.
5. A student registers for an event at most once and never beyond capacity. Duplicate gives "Already registered"; full gives "Event is full". Two simultaneous requests for the last seat: exactly one succeeds.
6. A student views and cancels their registrations. Cancelling frees the spot immediately.
7. A leader views participants of their own RSO's events and marks each registered student attended or not attended (correctable). Attendance cannot be recorded for unregistered students.
8. Each event shows registered count and attended count, always matching the database.

## Constraints
- Stack: HTML, CSS, JavaScript, Python Flask, SQLite only. Server-rendered pages with Jinja templates. Free, open-source packages only; no paid APIs, no API keys.
- Structure: routes call a service layer; services hold the rules and run without a browser; SQL stays in a data layer. Keep modules for auth, events, registration, attendance.
- Data tables: users, organizations, memberships, events, registrations, attendance. Registrations have UNIQUE(event_id, student_id). Registration runs in one BEGIN IMMEDIATE transaction that checks capacity before insert.
- Security: hash passwords (Werkzeug), HttpOnly SameSite session cookies, secret key from environment variable, CSRF token on all POST forms, validate all inputs, check roles and RSO membership on the server for every leader action.
- Accessibility: labeled form fields, keyboard-only use, readable text, usable at 360 px width.
- Privacy: fictional UNT-themed demo data only; attendance visible only to the owning RSO's leaders.
- Performance: listing and search under 1 second with 500 events and 5,000 registrations.
- AI features: none in the app.

## Out of scope
UNT login or UNT Engage integration, official RSO approvals or Talons Up points, payments or tickets, AI recommendations, native mobile apps, hosting, email or SMS reminders, scheduling-conflict detection.

## Quality expectations
- Automated pytest tests run with `uv run pytest`: duplicate registration, capacity limit, simultaneous last seat, cancel then re-register, role checks (student, pending leader, other-RSO leader), attendance rules, totals, password hashing.
- README.md with setup, seed, and run steps. Clear error messages. Small, readable modules.

## Acceptance checks
1. A student signs up, logs in, and sees upcoming events.
2. An approved leader creates an event and it appears in the listing; a student cannot open the create-event page (403).
3. A student registers once; a second attempt and an over-capacity attempt show errors.
4. A student cancels, and another student can then take the freed spot.
5. A leader records attendance and sees correct registered and attended totals; a leader of another RSO gets 403.
