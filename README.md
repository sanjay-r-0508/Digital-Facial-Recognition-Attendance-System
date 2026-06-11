# 🎭 AI-Powered Facial Recognition Attendance Management System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue">
  <img src="https://img.shields.io/badge/Flask-Web%20Framework-black">
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-green">
  <img src="https://img.shields.io/badge/Mediapipe-Face%20Detection-orange">
  <img src="https://img.shields.io/badge/Scikit--Learn-RandomForest-red">
  <img src="https://img.shields.io/badge/SQLite-Database-blue">
</p>

<p align="center">
<b>Intelligent Attendance Automation Using Computer Vision and Machine Learning</b>
</p>

<p align="center">
Automating student attendance through real-time facial recognition, machine learning, and web-based management.
</p>

---

# 📖 Overview

The AI-Powered Facial Recognition Attendance Management System is an intelligent attendance automation platform that eliminates manual attendance tracking by leveraging Computer Vision and Machine Learning.

The system captures student facial images, trains a machine learning model, recognizes students in real time, and automatically records attendance in a centralized database.

Unlike traditional attendance systems that rely on manual registers, RFID cards, or biometric devices, this solution provides a contactless, secure, and scalable approach to attendance management. 

---

# 📸 Application Preview

<p align="center">
  <img src="https://github.com/user-attachments/assets/e5b58429-70fa-4230-8d5c-47fc37f210e5" alt="AI Facial Recognition Attendance System" width="100%">
</p>

<p align="center">
<b>AI-Powered Facial Recognition Attendance Management Dashboard</b>
</p>

The dashboard provides a centralized interface for:

- 👨‍🎓 Student Registration
- 📸 Face Dataset Collection
- 🤖 Model Training
- 🎭 Real-Time Face Recognition
- 📝 Attendance Recording
- 📊 Attendance Analytics
- 📥 CSV Report Export

---

# 🚨 Problem Statement

Educational institutions often face challenges such as:

- Proxy attendance
- Manual attendance errors
- Time-consuming record keeping
- Attendance fraud
- Delayed reporting
- Difficulty managing large classrooms

Traditional methods are inefficient and prone to human error.

This project addresses these challenges by implementing a fully automated facial recognition-based attendance system capable of identifying students and recording attendance instantly. :contentReference[oaicite:2]{index=2}

---

# 🎯 Key Features

## 👨‍🎓 Student Registration

- Add Student Information
- Roll Number Management
- Class & Section Assignment
- Registration Number Tracking

---

## 📸 Face Dataset Collection

- Capture Multiple Student Images
- Automated Dataset Organization
- Student-wise Image Storage

---

## 🤖 AI Model Training

- Face Detection using MediaPipe
- Feature Extraction
- Embedding Generation
- Random Forest Classification

---

## 🎭 Face Recognition

- Real-Time Student Identification
- Confidence-Based Recognition
- Unknown Face Detection

---

## 📝 Attendance Management

- Automatic Attendance Marking
- Timestamp Recording
- Attendance History Tracking

---

## 📊 Analytics Dashboard

- Daily Attendance Trends
- Weekly Attendance Reports
- Monthly Attendance Reports
- Attendance Visualization

---

## 📥 Data Export

- CSV Export
- Attendance Records Download

---

# 🏗️ System Architecture

```text
Student Registration
          │
          ▼
Dataset Collection
          │
          ▼
Face Detection
          │
          ▼
Feature Extraction
          │
          ▼
Model Training
          │
          ▼
Random Forest Classifier
          │
          ▼
Face Recognition
          │
          ▼
Attendance Logging
          │
          ▼
Analytics Dashboard
```

---

# 🔄 System Workflow

```text
Register Student
       │
       ▼
Capture Face Images
       │
       ▼
Store Dataset
       │
       ▼
Train ML Model
       │
       ▼
Deploy Recognition Model
       │
       ▼
Recognize Student Face
       │
       ▼
Mark Attendance
       │
       ▼
Generate Reports
```

---

# 🧠 Machine Learning Pipeline

## Face Detection

The system uses MediaPipe Face Detection to identify facial regions within images before feature extraction. :contentReference[oaicite:3]{index=3}

---

## Feature Extraction

Each detected face is:

1. Cropped
2. Converted to grayscale
3. Resized to 32 × 32
4. Flattened into numerical embeddings

These embeddings become the input features for classification. :contentReference[oaicite:4]{index=4}

---

## Model Training

The system trains a:

### Random Forest Classifier

Configuration:

- 150 Trees
- Multi-core Processing
- Student ID Classification

The trained model is stored as:

```text
model.pkl
```

for future predictions. :contentReference[oaicite:5]{index=5}

---

## Recognition Process

```text
Input Face
     │
     ▼
Face Detection
     │
     ▼
Embedding Extraction
     │
     ▼
Random Forest Prediction
     │
     ▼
Confidence Evaluation
     │
     ▼
Attendance Marking
```

Recognition occurs only when confidence exceeds the configured threshold. 

---

# 🗄️ Database Design

The system uses SQLite as the backend database.

## Students Table

Stores:

- Student Name
- Roll Number
- Class
- Section
- Registration Number
- Creation Timestamp

---

## Attendance Table

Stores:

- Student ID
- Student Name
- Attendance Timestamp



---

# 📊 Dashboard Features

### Attendance Statistics

- Last 30 Days Attendance
- Daily Check-in Counts
- Attendance Trends

### Student Management

- View Students
- Delete Students
- Dataset Cleanup

### Attendance Records

- Daily View
- Weekly View
- Monthly View
- Complete History

### CSV Downloads

- Attendance Reports
- Historical Records

:contentReference[oaicite:8]{index=8}

---

# 📂 Project Structure

```text
AI-Facial-Recognition-Attendance-System/
│
├── dataset/
│   └── <student_id>/
│       ├── image1.jpg
│       ├── image2.jpg
│       └── ...
│
├── static/
├── templates/
│
├── attendance.db
├── train_status.json
├── model.pkl
│
├── app.py
├── model.py
├── requirements.txt
└── README.md
```

---

# 🛠 Technology Stack

| Category | Technology |
|-----------|------------|
| Programming Language | Python |
| Backend Framework | Flask |
| Computer Vision | OpenCV |
| Face Detection | MediaPipe |
| Machine Learning | Scikit-Learn |
| Classification Model | Random Forest |
| Database | SQLite |
| Frontend | HTML, CSS, JavaScript |

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/AI-Facial-Recognition-Attendance-System.git

cd AI-Facial-Recognition-Attendance-System
```

---

## Create Virtual Environment

```bash
python -m venv venv
```

---

## Activate Environment

### Windows

```bash
venv\Scripts\activate
```

### Linux/macOS

```bash
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install flask
pip install opencv-python
pip install mediapipe
pip install scikit-learn
pip install pandas
pip install numpy
```

---

## Run Application

```bash
python app.py
```

---

# 🌐 Application Access

```text
http://127.0.0.1:5000
```

---

# 📈 Future Enhancements

- Deep Learning Face Recognition (FaceNet)
- Mobile Application
- Multi-Camera Support
- Cloud Database Integration
- Student Portal
- Faculty Portal
- Face Mask Recognition
- Live Classroom Attendance

---

# 🎓 Learning Outcomes

This project demonstrates practical implementation of:

- Computer Vision
- Face Detection
- Machine Learning
- Flask Development
- Database Design
- Full Stack Development
- Attendance Automation
- AI-Based Recognition Systems

---

# 📬 Contact

**Sanjay R**

📧 Email: sanjayrao0508@gmail.com

💻 GitHub: https://github.com/sanjay-r-0508

🔗 LinkedIn: https://linkedin.com/in/sanjayr0508

---

# ⭐ Support

If you find this project useful:

⭐ Star the Repository

🍴 Fork the Repository

🚀 Contribute New Features

🎭 Explore AI-Based Attendance Automation

---

<p align="center">
<b>🎭 Transforming Attendance Management Through Artificial Intelligence 🎭</b>
</p>
