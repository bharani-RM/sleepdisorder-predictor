# 🧠 Sleep Disorder Predictor

### 🚀 ML Web App | Flask • Docker • CI/CD • AWS

<p align="center">
  <img src="screenshots/home.png" width="80%" />
</p>

<p align="center">
  <b>Predict sleep disorders using lifestyle data with explainable AI</b><br>
  Built with end-to-end deployment using CI/CD and Docker
</p>

---

## 🔗 Live Demo

👉 http://YOUR-EC2-IP:5000

---

## 🧩 Features

✨ Predicts sleep disorders (Insomnia, Sleep Apnea, etc.)
📊 Confidence score + risk level
🧠 SHAP-based explainability (feature impact)
💡 Personalized health recommendations
⚡ Fully automated CI/CD pipeline
🐳 Dockerized & cloud deployed

---

## 📸 Screenshots

### 🏠 Home Page

<p align="center">
  <img src="screenshots/home.png" width="70%" />
</p>

---

### 📊 Prediction Result

<p align="center">
  <img src="screenshots/result.png" width="70%" />
</p>

---

### 📈 Model Explanation (SHAP)

<p align="center">
  <img src="screenshots/dashboard.png" width="70%" />
</p>

---

## ⚙️ Tech Stack

| Category | Technology         |
| -------- | ------------------ |
| Backend  | Python, Flask      |
| ML       | Scikit-learn, SHAP |
| Data     | Pandas             |
| DevOps   | Docker, CI/CD      |
| Cloud    | AWS EC2            |

---

## 🔄 CI/CD Pipeline

```text
Code Push → GitHub Actions → Build Docker Image → Push to Docker Hub → Deploy to EC2
```

### 🚀 Optimizations Used

* ✔ Parallel jobs
* ✔ Docker layer caching
* ✔ Smaller base images
* ✔ Automated deployment
* ✔ Zero manual intervention

---

## 🐳 Docker Setup

### Build

```bash
docker build -t ml-app .
```

### Run

```bash
docker run -p 5000:5000 ml-app
```

---

## ☁️ Deployment (AWS EC2)

```bash
docker pull <your-dockerhub-username>/ml-app

docker run -d -p 5000:5000 \
  --restart=always \
  --name ml-app \
  <your-dockerhub-username>/ml-app
```

---

## 📂 Project Structure

```bash
.
├── app.py
├── requirements.txt
├── Dockerfile
├── datasets/
├── templates/
├── screenshots/
└── .github/workflows/deploy.yml
```

---

## 🧠 Model Details

* Algorithm: Random Forest
* Inputs:

  * Age
  * Gender
  * Sleep Duration
  * Physical Activity
  * BMI
  * Blood Pressure

---

## ⚠️ Common Issues

### App not opening

✔ Check EC2 security group (port 5000)

---

### Container not running

```bash
docker ps
docker logs ml-app
```

---

### Connection refused

✔ Ensure Flask runs on:

```python
app.run(host="0.0.0.0", port=5000)
```

---

## 🔥 Future Improvements

* 🌐 Custom domain + HTTPS
* 🔁 Auto rollback deployment
* 📊 Monitoring with Prometheus & Grafana
* ⚡ Blue-Green deployment
* ☁️ Serverless ML deployment

---

## 👨‍💻 Author

**Bharani RM**

---

## ⭐ Show your support

If you like this project, give it a ⭐ on GitHub!

