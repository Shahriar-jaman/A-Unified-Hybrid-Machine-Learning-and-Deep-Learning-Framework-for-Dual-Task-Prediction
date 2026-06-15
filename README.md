**Here is a clean, professional `README.md` for your AIMHESS project:**

```markdown
# AIMHESS - AI Mental Health & Educational Support System

**An intelligent web platform that predicts student academic performance and mental health stress levels using Machine Learning and Deep Learning, then provides personalized AI mentoring and daily planning.**

---

## ✨ Features

- **Dual-Platform Prediction Engine**
  - LightGBM Baseline Models
  - Multiple Deep Learning Models (MLP, CNN, LSTM, BiLSTM, Attention)
  - Academic Performance Prediction
  - Mental Health Stress Prediction

- **AI-Powered Chatbot Mentor** (Groq + Llama-3.3-70B)
  - Context-aware conversations using prediction results
  - Personalized academic and wellbeing guidance

- **AI-Generated Daily Planner**
  - Automatically creates personalized daily schedule based on performance & stress levels
  - Download as PDF

- **User Authentication**
  - Secure login/signup with MySQL

- **Beautiful Responsive UI**
  - Modern dark theme with Bootstrap 5

---

## 🛠️ Tech Stack

- **Backend**: Flask (Python)
- **Database**: MySQL
- **ML Models**: LightGBM, TensorFlow/Keras
- **AI**: Groq (Llama-3.3-70B)
- **Frontend**: Bootstrap 5, Font Awesome, Custom CSS
- **PDF Generation**: ReportLab
- **Others**: Joblib, Pandas, NumPy, python-dotenv

---

## 📁 Project Structure

```
aimhess/
├── app.py                      # Main Flask application
├── .env                        # Environment variables
├── saved_models/               # ML models & scalers
│   ├── lgb_acad.pkl
│   ├── lgb_mh.pkl
│   └── *.keras
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── home.html
│   ├── risk_questionnaire.html
│   ├── result.html
│   ├── chatbot.html
│   └── planner.html
├── static/
│   ├── css/
│   └── img/
└── README.md
```

---

## 🚀 Installation & Setup

### 1. Clone the Project
```bash
git clone <your-repo-url>
cd aimhess
```

### 2. Install Dependencies
```bash
pip install flask mysql-connector-python joblib numpy pandas python-dotenv groq tensorflow reportlab
```

### 3. Setup Environment Variables (`.env`)
```env
FLASK_SECRET_KEY=your-super-secret-key
GROQ_API_KEY=gsk_xxxxxxxxxxxxxxxxxxxxxxxx
DB_HOST=localhost
DB_USER=aimhes_user
DB_PASS=aimhes123
DB_NAME=aimhes_db
```

### 4. Database Setup
```sql
CREATE DATABASE aimhes_db;
CREATE USER 'aimhes_user'@'localhost' IDENTIFIED BY 'aimhes123';
GRANT ALL PRIVILEGES ON aimhes_db.* TO 'aimhes_user'@'localhost';
FLUSH PRIVILEGES;
```

Run the SQL script to create `users` table (you can add it later).

### 5. Run the Application
```bash
python app.py
```

Visit: `http://localhost:5001`

---

## 📋 How to Use

1. **Sign Up / Login**
2. Go to **Risk Assessment** → Fill the form → Submit
3. View your **Prediction Results**
4. Go to **AI Mentor** for personalized chat
5. Go to **Daily Planner** → AI generates custom schedule → Download PDF

---

## 🎯 Key Routes

- `/` → Landing Page
- `/login`, `/signup`
- `/risk` → Assessment Form
- `/result` → Prediction Results
- `/chatbot` → AI Mentor
- `/planner` → AI Daily Planner
- `/planner/pdf` → Download Planner

---

## 🧠 AI Features

- Chatbot has full access to your **Performance Level**, **Stress Level**, and **Scores**
- Daily Planner is **dynamically generated** by Llama-3.3-70B based on your predictions
- All suggestions are personalized

---

---

## 👨‍💻 Developers

- **MD Sakib Sarker**
- **Shahriar Jaman**

---

**Made with ❤️ for students' wellbeing and academic success.**

---
