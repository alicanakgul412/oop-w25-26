# 🎓 Student Projects Showcase App

## 🧠 Project Overview

The goal of this project is to build a **web application** that allows students to create their own profiles and showcase the projects they’ve built.  

Each student can add one or more projects, including a title, short description, image, and GitHub link.  
An **admin user** can log in to review all projects and **select the best ones** to display on the **public homepage**.

Project should be build in 2 phases (vibe coded Prototype and Python web app)
---

## 🚀 Core Features

### 👩‍🎓 Student Features
- Register and log in.
- Create and edit their profile:
  - Name / username  
  - Short bio  
  - GitHub link  
  - Optional profile picture  
- Add, edit, and delete their own projects:
  - Title  
  - Description  
  - Image  
  - GitHub link  

### 🧑‍💼 Admin Features
- Log in as admin.  
- View all student projects.  
- Mark or unmark projects as **featured**.  
- Featured projects appear on the public homepage.

### 🌐 Public Page
- Accessible without login.  
- Displays only featured projects.  
- Each project card includes:
  - Image  
  - Title  
  - Short description  
  - Student name  
  - GitHub link  

---

# Phase 1 - vibe coding
## Tech
Choose any vibe coding platform you like
* base44 (my preference)
* lovable.app
* replit

# Phase 2 - Python  
## ⚙️ Technical Requirements 

| Component | Technology |
|------------|-------------|
| Backend | **FastAPI** |
| Data validation | **Pydantic** |
| Database | **SQLite** (via SQLAlchemy)|
| Package manager | **uv** |
| Tests | **pytest** |
| Linter | **ruff** |
| Authentication | JWT-based |
| Frontend | HTML templates (Jinja2) |
| Styling | Bootstrap or Tailwind (optional) |
| Image handling | Local storage (`/uploads` folder) |

---

## 🧩 Suggested Data Models

### `Student`
| Field | Type | Description |
|-------|------|-------------|
| id | int | Primary key |
| username | str | Unique username |
| password | str | Hashed |
| bio | str | Short description |
| github_link | str | Optional GitHub profile link |
| avatar | str | Optional image path |

### `Project`
| Field | Type | Description |
|-------|------|-------------|
| id | int | Primary key |
| student_id | int | Foreign key → Student |
| title | str | Project title |
| description | str | Short description |
| github_link | str | GitHub repository URL |
| image | str | Optional image path |
| featured | bool | Whether project is public on homepage |

---

## 📁 Suggested Project Structure
```
student_projects/
│
├── app/
│ ├── main.py
│ ├── models.py
│ ├── schemas.py
│ ├── database.py
│ ├── routes/
│ │ ├── students.py
│ │ ├── projects.py
│ │ └── admin.py
│ └── templates/
│ ├── index.html
│ ├── student_profile.html
│ └── project_detail.html
│
├── uploads/
│
├── requirements.txt
└── README.md
```
