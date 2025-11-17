# Django To-Do List Application

A full-featured task management web application built with Django. This project implements user authentication, CRUD operations for tasks, and a clean, modern user interface.

> **Note:** This project was created by following the [Dennis Ivy Django To-Do List Tutorial](https://www.youtube.com/watch?v=llbtoQTt4qw). It serves as a learning project to understand Django's Class-Based Views, authentication system, and web application development.

## Features

- ✅ **User Authentication System**
  - User registration
  - Login/Logout functionality
  - User-specific task management
  
- 📝 **Task Management (CRUD Operations)**
  - Create new tasks with title and description
  - View all tasks in a list
  - Update/Edit existing tasks
  - Delete tasks
  - Mark tasks as complete/incomplete
  
- 🔍 **Search Functionality**
  - Search tasks by title
  - Real-time filtering
  
- 📊 **Task Statistics**
  - Display count of incomplete tasks
  - Visual indicators for task completion status
  
- 🎨 **Modern User Interface**
  - Clean and responsive design
  - Intuitive navigation
  - Visual feedback for task status

## Technology Stack

- **Backend:** Django 5.0.7
- **Database:** SQLite3 (default Django database)
- **Frontend:** HTML, CSS
- **Authentication:** Django's built-in authentication system
- **Python Version:** Python 3.x

### Dependencies

```
asgiref==3.8.1
Django==5.0.7
pillow==10.4.0
sqlparse==0.5.1
```

## Installation

### Prerequisites

- Python 3.x installed on your system
- pip (Python package installer)
- Virtual environment (recommended)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/MyroslavRepin/To-Do-list.git
   cd To-Do-list
   ```

2. **Create and activate a virtual environment** (recommended)
   
   On Windows:
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```
   
   On macOS/Linux:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (optional, for admin access)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   
   Open your web browser and navigate to:
   - Application: `http://127.0.0.1:8000/`
   - Admin panel: `http://127.0.0.1:8000/admin/`

## Usage

### Getting Started

1. **Register a new account** or **login** if you already have one
2. **Create tasks** by clicking the "+" button
3. **View all your tasks** on the main task list page
4. **Search tasks** using the search bar at the top
5. **Update tasks** by clicking on a task title
6. **Delete tasks** by clicking the "×" button next to a task
7. **Mark tasks as complete** by editing the task and checking the complete checkbox

### User Guide

- **Task List Page:** Displays all your tasks with completion status
- **Create Task:** Add a new task with a title and optional description
- **Edit Task:** Click on any task to view and edit its details
- **Delete Task:** Remove tasks you no longer need
- **Search:** Filter tasks by typing in the search box
- **Logout:** Sign out from your account using the logout button

## Project Structure

```
To-Do-list/
├── base/                      # Main Django app
│   ├── migrations/           # Database migrations
│   ├── templates/            # HTML templates
│   │   └── base/
│   │       ├── base.html     # Base template
│   │       ├── login.html    # Login page
│   │       ├── register.html # Registration page
│   │       ├── task_list.html # Main task list
│   │       ├── task.html     # Task detail view
│   │       ├── task_form.html # Create/Update form
│   │       └── task_confirm_delete.html
│   ├── admin.py              # Admin configuration
│   ├── models.py             # Data models (Task model)
│   ├── views.py              # View logic
│   ├── urls.py               # URL routing for app
│   └── tests.py              # Test cases
├── TODO_LIST/                # Project settings directory
│   ├── settings.py           # Django settings
│   ├── urls.py               # Main URL configuration
│   ├── wsgi.py               # WSGI configuration
│   └── asgi.py               # ASGI configuration
├── manage.py                 # Django management script
├── requirements.txt          # Project dependencies
└── README.md                 # Project documentation
```

## Database Schema

### Task Model

| Field | Type | Description |
|-------|------|-------------|
| id | AutoField | Primary key |
| user | ForeignKey | Associated user (auth.User) |
| title | CharField(200) | Task title |
| description | TextField | Task description (optional) |
| complete | BooleanField | Completion status |
| create | DateTimeField | Creation timestamp |

## Tutorial Credit

This project was created by following the **Django To-Do List App Tutorial** by Dennis Ivy:
- 📺 [YouTube Tutorial](https://www.youtube.com/watch?v=llbtoQTt4qw)
- 👨‍💻 [Dennis Ivy's Channel](https://www.youtube.com/c/DennisIvy)

The tutorial provides an excellent introduction to:
- Django Class-Based Views (ListView, DetailView, CreateView, UpdateView, DeleteView)
- Django authentication system
- Template inheritance
- CRUD operations
- User-specific data filtering

## Contributing

This is a learning project, but suggestions and improvements are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Security Note

⚠️ **Important:** This project contains a publicly visible `SECRET_KEY` in `settings.py` and has `DEBUG = True`. These are fine for learning and development purposes, but **must be changed** before deploying to production:

1. Generate a new secret key
2. Set `DEBUG = False`
3. Configure `ALLOWED_HOSTS` properly
4. Use environment variables for sensitive data

## License

This project is open source and available for educational purposes. Please refer to the original tutorial creator (Dennis Ivy) for any specific licensing questions.

## Contact

Project Link: [https://github.com/MyroslavRepin/To-Do-list](https://github.com/MyroslavRepin/To-Do-list)

---

**Happy Coding! 🚀**
