# Student Guidance System

A Django-based REST API for student guidance and support management system.

## 🚀 Features

- User authentication with JWT tokens
- Django REST Framework for API development
- PostgreSQL database integration
- Student and guidance management
- Token-based authentication with refresh tokens

## 📋 Requirements

- Python 3.9+
- PostgreSQL 18
- Django 4.2.30
- Django REST Framework 3.16.1

## 📦 Installation

### 1. Clone the Repository
```bash
git clone git@github.com:Princexhy07/Student_Guidance_System.git
cd Student-Guidance-System
```

### 2. Create Virtual Environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Environment Configuration
Create a `.env` file based on `.env.example`:
```env
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost

DB_ENGINE=django.db.backends.postgresql
DB_NAME=student_guidance_db
DB_USER=postgres
DB_PASSWORD=your-password
DB_HOST=localhost
DB_PORT=5432
```

### 5. Database Setup
```bash
python manage.py migrate
python manage.py createsuperuser
```

### 6. Run Development Server
```bash
python manage.py runserver
```

The API will be available at `http://localhost:8000`

## 📚 API Documentation

- Admin Panel: `http://localhost:8000/admin`
- API: `http://localhost:8000/api/`

## 🏗️ Project Structure

```
Student-Guidance-System/
├── authentication/          # User authentication & JWT tokens
├── base/                   # Base models and utilities
├── course/                 # Course management
├── student_guidance_system/  # Project settings
├── manage.py               # Django management script
├── requirements.txt        # Python dependencies
└── .env.example            # Environment variables template
```

## 🔐 Authentication

The API uses JWT (JSON Web Tokens) for authentication:
- Access Token: 15 minutes expiry
- Refresh Token: 7 days expiry
- Token Blacklist support for logout

## 📝 License

MIT License

## 👤 Author

Princexhy07

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
