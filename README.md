# 🐍 Flask Docker App

<p align="center">

<img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-3.x-000000?style=for-the-badge&logo=flask&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-Environment-FCC624?style=for-the-badge&logo=linux&logoColor=black"/>

</p>

<p align="center">
  <b>🚀 A Flask Web Application Containerized with Docker</b>
</p>

<p align="center">
  A hands-on project demonstrating how to build, containerize, and run a Python Flask application using Docker.
</p>

---

## 📌 About

**Flask Docker App** is a simple Python web application built using **Flask** and containerized using **Docker**.

The project demonstrates the basic containerization workflow:

```text
🐍 Flask Application
        ↓
🐳 Dockerfile
        ↓
📦 Docker Image
        ↓
🚢 Docker Container
        ↓
🌐 Web Application
```

This project was created to gain practical experience with **Docker and Python web applications**.

---

## ✨ Features

* 🐍 Simple Flask web application
* 🐳 Docker containerization
* 📦 Docker image creation
* 🚢 Container management
* 🌐 Port mapping
* 💻 Docker CLI practice
* 🔍 Container log monitoring
* ⚙️ Basic application deployment workflow

---

## 🛠️ Technologies Used

| Technology            | Purpose                      |
| --------------------- | ---------------------------- |
| 🐍 **Python 3.12**    | Application development      |
| 🌶️ **Flask**         | Python web framework         |
| 🐳 **Docker**         | Application containerization |
| 🐧 **Linux / Ubuntu** | Development environment      |

---

## 📂 Project Structure

```text
flask-docker-app/
│
├── 🐍 app.py
├── 🐳 Dockerfile
└── 📖 README.md
```

### 📄 File Description

| File         | Description                            |
| ------------ | -------------------------------------- |
| `app.py`     | Contains the Flask application         |
| `Dockerfile` | Defines the Docker image configuration |
| `README.md`  | Project documentation                  |

---

## 🐍 Flask Application

The application contains a basic home route that returns a simple message.

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello! Flask application is running successfully inside Docker."

app.run(host="0.0.0.0", port=5000)
```

### 🌐 Application Endpoint

```text
GET /
```

### 📤 Response

```text
Hello! Flask application is running successfully inside Docker.
```

---

# 🐳 Docker Configuration

## Dockerfile

```dockerfile
FROM python:3.12

WORKDIR /app

COPY . .

RUN pip install flask

EXPOSE 5000

CMD ["python", "app.py"]
```

---

## 🔎 Dockerfile Explanation

| Instruction             | Purpose                                    |
| ----------------------- | ------------------------------------------ |
| `FROM python:3.12`      | 🐍 Uses Python 3.12 as the base image      |
| `WORKDIR /app`          | 📁 Sets `/app` as the working directory    |
| `COPY . .`              | 📋 Copies project files into the container |
| `RUN pip install flask` | 📦 Installs Flask                          |
| `EXPOSE 5000`           | 🌐 Documents the Flask application port    |
| `CMD`                   | 🚀 Starts the Flask application            |

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/atharva00771/flask-docker-app.git
```

```bash
cd flask-docker-app
```

---

## 2️⃣ Build the Docker Image

```bash
docker build -t flask-app .
```

The `-t` option assigns the name `flask-app` to the Docker image.

---

## 3️⃣ Verify the Image

```bash
docker images
```

You should see:

```text
flask-app
```

---

## 4️⃣ Run the Container

```bash
docker run -d -p 5000:5000 --name flask-container flask-app
```

### 🔍 Command Breakdown

```text
-d
↓
Runs container in detached mode

-p 5000:5000
↓
Maps host port 5000 to container port 5000

--name flask-container
↓
Assigns a name to the container

flask-app
↓
Docker image used to create the container
```

---

## 5️⃣ Check Running Containers

```bash
docker ps
```

The Flask container should appear in the list.

---

## 6️⃣ Access the Application

Open your browser:

```text
http://localhost:5000
```

### ✅ Expected Output

```text
Hello! Flask application is running successfully inside Docker.
```

---

# 🔍 Docker Commands

### 📦 View Images

```bash
docker images
```

### 🚢 View Running Containers

```bash
docker ps
```

### 📋 View All Containers

```bash
docker ps -a
```

### 📜 View Container Logs

```bash
docker logs flask-container
```

### ⛔ Stop Container

```bash
docker stop flask-container
```

### 🗑️ Remove Container

```bash
docker rm flask-container
```

### 🗑️ Remove Image

```bash
docker rmi flask-app
```

---

# 🧪 Project Workflow

```text
        👨‍💻 Write Flask Code
                 │
                 ▼
            📄 app.py
                 │
                 ▼
          🐳 Create Dockerfile
                 │
                 ▼
        📦 Build Docker Image
                 │
                 ▼
       🚢 Run Docker Container
                 │
                 ▼
        🌐 localhost:5000
```

---

# 📚 What I Learned

Through this project, I practiced:

* 🐍 Creating a Flask application
* 🐳 Writing a Dockerfile
* 📦 Building Docker images
* 🚢 Running Docker containers
* 🔗 Understanding port mapping
* 📋 Managing containers using Docker CLI
* 📜 Checking container logs
* 🌐 Running a Python web application inside Docker

---

# 🎯 Learning Objective

The objective of this project is to understand the fundamentals of **containerizing Python web applications** and to gain practical experience with the Docker workflow:

**Code → Dockerfile → Image → Container → Application**

---

# 🔮 Future Improvements

Possible improvements for this project:

* 🔹 Add `requirements.txt`
* 🔹 Use a production WSGI server such as Gunicorn
* 🔹 Add environment variables
* 🔹 Add Docker Compose
* 🔹 Add application health checks
* 🔹 Deploy the container to AWS

---

# 👨‍💻 Author

## **Atharva Avhad**

🎓 **B.Tech AI & Data Science Student**
📊 **Aspiring Data Analyst**
☁️ **AWS Cloud Enthusiast**
🐳 **Learning Docker & Cloud Technologies**

<p>
<a href="https://github.com/atharva00771">
<img src="https://img.shields.io/badge/GitHub-Atharva00771-181717?style=for-the-badge&logo=github"/>
</a>
</p>

---

## ⭐ Support

If you found this project useful, consider giving the repository a ⭐.

<p align="center">

### 🐍 Flask + 🐳 Docker = 🚀

**Learning by Building • Building by Practicing**

</p>
