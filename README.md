# task-manager
# Task Manager

A simple, secure task management web app built with Django. Users can sign up, log in, and manage their own personal to-do list — create, edit, mark complete, and delete tasks.

## Features

- User authentication (sign up, login, logout)
- Each user only sees and manages their own tasks
- Create, edit, complete, and delete tasks
- Tasks support a title, description, due date, and completion status
- Clean, responsive UI built with Bootstrap
- Django admin panel for managing data directly

## Tech Stack

- **Backend:** Python, Django
- **Database:** SQLite (development)
- **Frontend:** Django Templates, Bootstrap 5
- **Auth:** Django's built-in authentication system

## Getting Started

### Prerequisites

- Python 3.10+
- pip

### Installation

1. Clone the repository
   ```bash
   git clone <your-repo-url>
   cd task-manager/task_manager_project
   ```

2. Create and activate a virtual environment
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. Install dependencies
   ```bash
   pip install django
   ```

4. Apply database migrations
   ```bash
   python manage.py migrate
   ```

5. Create an admin account (optional, for the Django admin panel)
   ```bash
   python manage.py createsuperuser
   ```

6. Run the development server
   ```bash
   python manage.py runserver
   ```

7. Open your browser to `http://127.0.0.1:8000/`

## Usage

- Visit `/signup/` to create a new account
- Visit `/login/` to log in
- Once logged in, you'll land on your task list where you can add, edit, complete, and delete tasks
- Visit `/admin/` to access the Django admin panel (requires a superuser account)

## Project Structure

```
task_manager_project/
├── config/             # Project settings and root URL configuration
├── tasks/              # Main app: models, views, forms, URLs
├── templates/          # HTML templates
│   ├── registration/   # Login and signup pages
│   └── tasks/          # Task list, form, and delete confirmation pages
├── manage.py
└── README.md
```

## Security Notes

- Each task is tied to an owner; users cannot view or modify another user's tasks
- All forms are protected against CSRF attacks
- Passwords are hashed using Django's built-in authentication system

## License

This project is open source and available for personal or educational use.
