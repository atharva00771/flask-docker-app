🐍 Flask Docker App

<p align="center">
<img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.12"/>
<img src="https://img.shields.io/badge/Flask-3.x-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask 3.x"/>
<img src="https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
<img src="https://img.shields.io/badge/Linux-Ubuntu-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux Ubuntu"/>
</p>

<p align="center">
<b>🚀 Flask Web Application Containerized with Docker</b>
</p>

<p align="center">
A beginner-friendly project demonstrating how to build, containerize, and run a Python Flask application using Docker.
</p>

📌 About

Flask Docker App is a simple Python web application developed using Flask and containerized using Docker.

This project demonstrates the basic Docker workflow:

🐍 Flask Application
        ↓
🐳 Dockerfile
        ↓
📦 Docker Image
        ↓
🚢 Docker Container
        ↓
🌐 Web Application


This project was created to gain hands-on experience with Python, Flask, Docker, Linux, containers, images, and port mapping.

✨ Features
🐍 Simple Flask web application
🐳 Docker containerization
📦 Docker image creation
🚢 Docker container management
🌐 Port mapping
💻 Docker CLI practice
🔍 Container log monitoring
⚙️ Basic application deployment workflow
🛠️ Technologies Used
Technology	Purpose
🐍 Python 3.12	Application development
🌶️ Flask 3.x	Python web framework
🐳 Docker	Application containerization
🐧 Ubuntu/Linux	Development environment
📂 Project Structure
flask-docker-app/
├── app.py
├── Dockerfile
├── requirements.txt
└── README.md

📄 File Description
File	Description
app.py	Contains the Flask application
Dockerfile	Defines the Docker image configuration
requirements.txt	Contains Python dependencies
README.md	Project documentation
🐍 Flask Application

The application contains a home route that returns a welcome message when accessed through a browser.

File: app.py

from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello! Flask App is Running Inside Docker 🚀"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)

📦 Requirements

File: requirements.txt

Flask==3.1.0

🐳 Dockerfile

The Dockerfile defines the instructions required to build the Docker image.

FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

EXPOSE 500
