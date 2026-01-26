# GoldenQA – Q&A Platform

GoldenQA is a modern, user-friendly Question & Answer (Q&A) web platform built with Django. Users can ask questions, post answers, and interact through a voting system, all organized under clear and meaningful categories.

The goal of this project is to demonstrate a complete, cleanly structured Django application with real-world features such as authentication, relational data models, and interactive UI elements.

---

## Features

- User authentication (sign up, login, logout)
- Ask questions with category tags
- Answer existing questions
- Upvote and downvote answers
- Category-based filtering (16 categories)
- Sort questions by newest or most answered
- Clean and modern UI using Google Fonts (Poppins)

---

## Categories

- Daily Life
- Sports
- Hobbies
- Technology
- Education and Career
- Health and Fitness
- Travel
- Entertainment
- Food and Cooking
- Music and Arts
- Books and Literature
- Relationships
- Gaming
- Science and Nature
- Philosophy
- Other

---

## Technologies

- Backend: Django 4.2.20
- Database: SQLite3
- Frontend: HTML, CSS, JavaScript
- Fonts: Google Fonts (Poppins)

---

## Installation

### Requirements

- Python 3.9+
- pip

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/nehiriremcelik/WEB.git
   cd WEB
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```

3. Activate the virtual environment:

   Windows:
   ```bash
   venv\Scripts\activate
   ```

   Linux / macOS:
   ```bash
   source venv/bin/activate
   ```

4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

5. Apply database migrations:
   ```bash
   python manage.py migrate
   ```

6. (Optional) Create a superuser:
   ```bash
   python manage.py createsuperuser
   ```

7. Run the development server:
   ```bash
   python manage.py runserver
   ```

8. Open in your browser:
   ```
   http://127.0.0.1:8000/
   ```

---

## Project Structure

```
WEB/
├── goldenqa/
│   ├── models.py
│   ├── views.py
│   ├── forms.py
│   ├── urls.py
│   ├── validators.py
│   ├── templates/
│   │   └── cores/
│   │       ├── base.html
│   │       ├── home.html
│   │       ├── login.html
│   │       ├── signup.html
│   │       └── question_detail.html
│   └── static/
├── cores/
├── WEB/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── db.sqlite3
├── manage.py
└── requirements.txt
```

---

## Usage

### User Registration

- Create an account using the Sign Up page
- Password must be at least 8 characters and include letters and numbers

### Asking Questions

- Log in
- Write your question
- Select a category and submit

### Answering Questions

- Open a question detail page
- Write and submit your answer

### Voting

- Use upvote or downvote buttons on answers
- Votes update instantly

### Filtering and Sorting

- Filter questions by category
- Sort by newest or most answered

---

## Security Notes

For production environments:

- Set DEBUG = False
- Store SECRET_KEY securely
- Configure ALLOWED_HOSTS
- Use HTTPS
- Use a production-ready database such as PostgreSQL or MySQL

---

## Database Models

### Question

- user
- text
- tag
- created_at

### Answer

- user
- question
- content
- created_at

### Vote

- user
- answer
- created_at

---

## License

This project is open source and intended for educational use.
