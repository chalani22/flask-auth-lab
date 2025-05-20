# Flask Authentication System 🔐

A simple authentication system built with Python, Flask, SQLite, and JSON Web Tokens (JWT).
It allows users to register, log in, and access protected content via secure tokens.

---

## 🚀 Features

* User registration with hashed passwords
* User login using JWT-based sessions
* Protected route requiring authentication
* Flash messages for user feedback
* Password hashing using SHA-256
* JWT token expiration after 30 minutes

---

## 📂 Project Structure

```
auth_lab/
│
├── app.py               # Main Flask application
├── users.db             # SQLite database (auto-created)
├── templates/           # HTML templates
│   ├── home.html
│   ├── register.html
│   ├── login.html
│   └── protected.html
├── static/              # (Optional) For CSS styles
│   └── style.css
└── venv/                # Virtual environment (not pushed to Git)
```

---

## 🔧 Setup Instructions

### 1. Create & Activate Virtual Environment

```bash
# Create virtual environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate

# On macOS/Linux:
source venv/bin/activate
```

### 2. Install Dependencies

```bash
pip install Flask PyJWT
```

### 3. Run the App

```bash
python app.py
```

Then visit: [http://127.0.0.1:3000](http://127.0.0.1:3000)

---

## 🧪 How to Use

1. Go to `/register` and create a new user.
2. Log in at `/login` with valid credentials.
3. You'll be redirected to the protected page at `/protected`.
4. Trying to access `/protected` without logging in redirects to `/login`.
5. JWT session expires in 30 minutes.

---

## 🛡️ Security Notes

* Passwords are hashed using SHA-256 (not recommended for production).
* For production, use `bcrypt` or `argon2` for secure password storage.
* JWT is stored in an HTTP-only cookie to prevent access from JavaScript.
* The JWT secret key should be stored securely (e.g., in an `.env` file).

---

## 📜 License

This project is for educational use and does not include a license by default.
