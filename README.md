#Django To-Do App (Dockerized)

A simple To-Do List application built with Django and containerized with Docker.

Features

Add, toggle ✅, and delete ❌ tasks

Django Admin interface

SQLite database

Fully containerized with Docker

Auto migrations & optional auto-superusertodoproject/
│── Dockerfile
│── entrypoint.sh
│── requirements.txt
│── manage.py

├── todoproject/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
│
└── todo/
    ├── models.py
    ├── views.py
    ├── urls.py
    ├── forms.py
    ├── admin.py
    └── templates/todo/
        ├── base.html
        └── index.html
        
#Build the Docker image
docker build -t django-todo .

Run the container
docker run -d -p 8000:8000 django-todo:latest 

Automatic Migrations

The container automatically runs:

makemigrations

migrate

So you don’t need to run them manually.

<img width="1514" height="753" alt="Screenshot from 2025-08-19 20-44-45" src="https://github.com/user-attachments/assets/ceab05cb-17e3-4e7c-9253-d6206b4025fc" />


