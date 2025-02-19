# 🚀 Docker_Mlmodel

## 🌟 Overview
Docker_Mlmodel is a structured project demonstrating how to containerize a machine learning model using Docker. This setup ensures scalability, portability, and efficient model deployment.

---

## 📂 Project Structure
```bash
📂 Docker_Mlmodel
│── 📂 app/                  # Contains ML model and application logic
│   ├── 📜 model/            # Directory for trained models
│   ├── 📜 main.py           # API entry point for model inference
│   ├── 📜 requirements.txt  # Python dependencies
│── 📜 Dockerfile            # Docker configuration file
│── 📖 README.md             # Project documentation
│── 📜 .dockerignore         # Files to ignore in the Docker build
```

---

## 🔧 Prerequisites
Before getting started, ensure you have:
- 🐳 Docker installed
- 🐍 Python (if running locally)
- Required dependencies from `requirements.txt`

---

## 🚀 Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/AnushkaSharma2024/Docker_Mlmodel.git
cd Docker_Mlmodel
```

### 2️⃣ Build the Docker Image
Docker will create an image based on the `Dockerfile`, setting up the necessary environment.
```bash
docker build -t mlmodel-app .
```

### 3️⃣ Run the Docker Container
Execute the container and expose it on port 5000.
```bash
docker run -p 5000:5000 mlmodel-app
```

---

## 🛠️ How It Works
- The `Dockerfile` is based on a lightweight Python image.
- It installs dependencies from `requirements.txt`.
- It copies the ML model and application files.
- When the container starts, it runs `main.py`, serving an API for predictions.

---

## 🔄 Stopping & Cleaning Up
### Checking Running Containers
To view active Docker containers:
```bash
docker ps
```
To stop a running container:
```bash
docker stop <container_id>
```

### Removing Unused Docker Images
Clean up unnecessary images:
```bash
docker image prune -a
```

---

## 📜 Dockerfile
Below is the content of the `Dockerfile` used in this project:
```Dockerfile
FROM python:3.9-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

CMD ["python", "main.py"]
```

---

## 🙌 Thank You!
Thank you for exploring Docker_Mlmodel! If you have any questions or suggestions, feel free to reach out. 🚀
