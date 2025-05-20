
# Flask Authentication System 🔐

A simple authentication system built with Python, Flask, SQLite, and JSON Web Tokens (JWT).  
It allows users to register, log in, and access protected content via secure tokens.

---

## 🚀 Features

- User Registration with hashed passwords
- User Login with JWT-based session
- Protected Route requiring authentication
- Flash messages for user feedback
- Password hashing using SHA-256
- JWT-based session management with 30-minute expiration

---

## 🗂️ Project Structure

auth\_lab/
│
├── app.py               # Main Flask application
├── users.db             # SQLite database (auto-created)
├── templates/           # HTML templates
│   ├── home.html
│   ├── register.html
│   ├── login.html
│   └── protected.html
├── static/              # (Optional) For CSS if using
│   └── style.css

---

## 🔧 Setup Instructions

### 1.Create & Activate Virtual Environment

# Create virtual env
python -m venv venv

# Activate it
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate


### 2. Install Dependencies
pip install Flask PyJWT

### 4. Run the App
python app.py


Then open [http://127.0.0.1:3000](http://127.0.0.1:3000) in your browser.

---

## 🧪 How to Use

1. Register a new user via `/register`
2. Log in at `/login`
3. Get redirected to the protected page `/protected`
4. Accessing `/protected` without login redirects to `/login`
5. Token expires in 30 minutes

---

## 🛡️ Security Notes

* Passwords are hashed using SHA-256 (not suitable for production; use bcrypt/argon2 in real apps).
* JWT is stored in HTTP-only cookie.
* Secret key should be stored securely (e.g., in `.env`).

---
