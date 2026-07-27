<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Student%20Performance%20Predictor&fontSize=42&fontColor=fff&animation=twinkling&fontAlignY=32&desc=AI-Powered%20Academic%20Outcome%20Prediction%20System&descAlignY=52&descSize=16" />

<br/>

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Random Forest](https://img.shields.io/badge/Model-Random%20Forest-228B22?style=for-the-badge&logo=leaflet&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-A855F7?style=for-the-badge)](LICENSE)

<br/>

> **"Predict student academic outcomes before it's too late — using the power of Machine Learning."**

<br/>

[🚀 Quick Start](#-quick-start) • [📊 Features](#-features) • [🧠 How It Works](#-how-it-works) • [📁 Project Structure](#-project-structure) • [💻 Usage](#-usage)

</div>

---

## 🎯 Overview

The **Student Performance Predictor** is a machine learning-powered system that analyzes key academic and personal factors to predict whether a student will **Pass or Fail** a semester. Built with a Random Forest Classifier, it leverages multi-dimensional student data to enable educators and students to take **early, informed action**.

This system ingests data like study habits, attendance, internal marks, CGPA history, and socio-academic factors to produce a decisive prediction — making it a valuable tool for **academic advisors, institutions, and self-aware learners alike.**

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🤖 Smart Prediction Engine
Utilizes a **Random Forest Classifier** trained on multi-feature student data to deliver highly accurate Pass/Fail predictions.

</td>
<td width="50%">

### 🔢 Multi-Factor Analysis
Considers **8 key features** spanning demographics, study behavior, academic history, and socio-economic context.

</td>
</tr>
<tr>
<td width="50%">

### 💾 Persistent Model Storage
Trained models and label encoders are serialized using **joblib** for instant inference—no retraining required.

</td>
<td width="50%">

### 🖥️ Interactive CLI
A clean, intuitive **command-line interface** that walks users through entering student details and returns an instant prediction.

</td>
</tr>
</table>

---

## 🧠 How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    STUDENT DATA INPUT                           │
│  Gender · Age · Study Hours · Attendance · Internal Marks       │
│  Previous CGPA · Extra Courses · Family Support                 │
└────────────────────────┬────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────────────┐
│               DATA PREPROCESSING                                │
│  Label Encoding (Gender, Extra Courses, Family Support)         │
│  Feature Vector Assembly → NumPy Array                          │
└────────────────────────┬────────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────────────┐
│             RANDOM FOREST CLASSIFIER                            │
│  100 Decision Trees · Ensemble Voting · Majority Decision       │
└────────────────────────┬────────────────────────────────────────┘
                         │
                         ▼
              ┌──────────┴──────────┐
              │                     │
           ✅ PASS              ❌ FAIL
```

---

## 📊 Dataset Features

| Feature | Type | Description |
|---|---|---|
| `gender` | Categorical | Student's gender (`Male` / `Female`) |
| `age` | Numerical | Student's age in years |
| `study_hours_per_day` | Numerical | Average daily study hours |
| `attendance_percentage` | Numerical | Percentage of classes attended |
| `internal_marks` | Numerical | Internal assessment marks (out of 40) |
| `previous_sem_cgpa` | Numerical | CGPA of the previous semester |
| `extra_courses` | Categorical | Enrolled in extra courses (`Yes` / `No`) |
| `family_support` | Categorical | Has family academic support (`Yes` / `No`) |
| `result` | **Target** | Predicted outcome (`Pass` / `Fail`) |

---

## 📁 Project Structure

```
📦 Student Prediction System
├── 📄 students.csv              # Training dataset with student records
├── 🐍 train_model.py            # Model training, evaluation & serialization
├── 🐍 predict_student.py        # Interactive CLI for real-time predictions
├── 🤖 student_model.pkl         # Serialized trained Random Forest model
├── 🔤 label_encoders.pkl        # Serialized label encoders for categories
└── 📖 README.md                 # You are here
```

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/student-prediction-system.git
cd student-prediction-system
```

### 2. Set Up a Virtual Environment *(Recommended)*
```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 💻 Usage

### 🏋️ Step 1: Train the Model
Run the training script to process the dataset, train the classifier, and save the model artifacts.

```bash
python train_model.py
```

**Expected Output:**
```
Accuracy: 0.97
Classification Report:
              precision    recall  f1-score   support
        Fail       0.97      0.97      0.97        ...
        Pass       0.97      0.97      0.97        ...
Model and encoders saved successfully.
```

### 🔮 Step 2: Run a Prediction
Launch the interactive predictor and enter student details as prompted:

```bash
python predict_student.py
```

**Example Session:**
```
Enter student details for prediction:

Gender (Male/Female): Male
Age: 20
Study hours per day: 3
Attendance percentage: 85
Internal marks (out of 40): 32
Previous semester CGPA: 7.8
Extra courses (Yes/No): Yes
Family support (Yes/No): Yes

Predicted Result: Pass ✅
```

---

## ⚙️ Requirements

```
pandas
numpy
scikit-learn
joblib
```

Create a `requirements.txt` and install:
```bash
pip install pandas numpy scikit-learn joblib
```

---

## 🗺️ Roadmap

- [x] Core Random Forest classification model
- [x] Label encoding for categorical features
- [x] Interactive CLI predictor
- [x] Model persistence with joblib
- [ ] Flask/FastAPI REST endpoint for web deployment
- [ ] Feature importance visualization dashboard
- [ ] Expanded dataset with 500+ student records
- [ ] Support for multi-class outcome (Distinction, Pass, Fail, Backlog)

---

## 👨‍💻 Author

<div align="center">

**Tushar Rana**

[![GitHub](https://img.shields.io/badge/GitHub-tusharrana-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/YOUR_USERNAME)

</div>

---

## 📝 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute it.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" />

*Built with ❤️ and Python — Empowering Students with Predictive Intelligence*

</div>
