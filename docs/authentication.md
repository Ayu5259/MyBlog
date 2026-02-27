Project Authentication System

This project uses the built-in authentication scaffolding provided by Laravel through Auth::routes().
Authentication is session-based.

---

Registration Flow:

    User submits registration form.
    Input is validated.
    Password is hashed before saving.
    A new record is created in users table.
    User is automatically logged in.
    Redirected to /home.

Login Flow:

    User submits email and password.
    Credentials are checked.
    If valid, a session is created.
    User is redirected to /home.

Logout Flow:

    Session is invalidated.
    User is redirected to login page.

---

Auth::routes():
GET /login
POST /login
GET /register
POST /register
POST /logout
GET /password/reset
POST /password/email
POST /password/reset

---

Database:

Users Table Structure:
id
name
email (unique)
password (hashed)
remember_token
timestamps
(Passwords are stored as hashed values and never saved in plain text.)

---

Limitations:

No role-based access control.
No email verification enabled.
No multi-factor authentication.

---

Refactor the layouts in future:

components/navbar.blade.php
components/footer.blade.php
layouts/app.blade.php
