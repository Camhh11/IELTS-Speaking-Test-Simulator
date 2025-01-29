# IELTS-Speaking-Test-Simulator
This project is an IELTS Speaking Test Simulator designed to allow users to practice their   speaking skills for the IELTS test. The tool uses a combination of Flutter for the frontend and  Python with FastAPI for the backend, integrated with an LLM (Large Language Model) for  generating feedback.
# 🗣️ IELTS Speaking Test Simulator

![Flutter](https://img.shields.io/badge/Flutter-v3.16.0-blue?logo=flutter) 
![FastAPI](https://img.shields.io/badge/FastAPI-v0.109.0-green?logo=fastapi) 
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)

## 📌 Overview

This is a **full IELTS Speaking Test Simulator** designed to help users practice their speaking skills. The app provides **real-time speech-to-text conversion, AI-generated feedback**, and a **full IELTS test simulation**. 

🚀 **Tech Stack**:
- **Frontend**: Flutter (Android)
- **Backend**: FastAPI (Python) + OpenAI GPT-4o-mini for feedback
- **Speech-to-Text**: Google Cloud Speech-to-Text API

---

## 📂 Project Structure

ielts-speaking-app/ │── frontend/ # Flutter Android app │ ├── lib/ # Dart source code │ ├── assets/ # Images, audio files │ ├── pubspec.yaml # Flutter dependencies │ ├── android/ # Android build files │ ├── main.dart # Entry point of Flutter app │ │── backend/ # FastAPI backend │ ├── app/ # Source code │ │ ├── main.py # API entry point │ │ ├── models.py # Data models │ │ ├── routes.py # API endpoints │ ├── requirements.txt # Python dependencies │ ├── .env # API keys (ignored in Git) │ │── docs/ # Documentation │ ├── API_endpoints.md │ ├── setup_guide.md │ │── .gitignore # Ignore unnecessary files │── README.md # This file

## 🛠️ Setup Guide

### **🔹 Prerequisites**
Before running the app, ensure you have:
- **Flutter SDK** installed → [Download](https://flutter.dev/docs/get-started/install)
- **Python 3.10+** installed → [Download](https://www.python.org/downloads/)
- **Node.js & npm (Optional for API Testing)** → [Download](https://nodejs.org/)

---

### **🚀 Backend Setup (FastAPI)**
1. **Navigate to the backend folder**:
   ```bash
   cd backend
Create a virtual environment (optional but recommended):

bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate      # Windows
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Set up environment variables:

Create a .env file in the backend directory:
ini
Copy
Edit
OPENAI_API_KEY=your_openai_api_key
GOOGLE_SPEECH_CREDENTIALS=your_google_credentials.json
Run the server:

bash
Copy
Edit
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
Test the API in Swagger UI:

Open in browser: http://localhost:8000/docs



 Frontend Setup (Flutter)
Navigate to the frontend folder:

bash
Copy
Edit
cd frontend
Install Flutter dependencies:

bash
Copy
Edit
flutter pub get
Run the app on an Android device/emulator:

bash
Copy
Edit
flutter run
Ensure the backend is running, so the Flutter app can fetch feedback.

🎤 Features
✅ Speech-to-Text: Uses Google Cloud to transcribe spoken words.
✅ AI Feedback: OpenAI GPT-4o-mini provides IELTS-style feedback.
✅ Practice & Test Mode: Instant feedback or full test simulation.
✅ PDF Export: Save your results in a PDF for future practice.
✅ Real-Time Feedback: Immediate evaluation after each response.

📡 Deployment Guide
🌍 Deploy Backend to Render
Push your backend code to GitHub.
Sign in to Render and create a new web service.
Connect your GitHub repository and set:
Runtime: Python 3.x
Start Command: uvicorn app.main:app --host 0.0.0.0 --port 8000
Add environment variables (same as .env file).
Deploy & get a public backend URL.
📲 Deploy Flutter App
Android Deployment:
bash
Copy
Edit
flutter build apk
Upload to Google Play Store or share app-release.apk directly.
🔥 API Endpoints
📌 The backend provides RESTful APIs.

POST /feedback → Generates IELTS-style feedback.
json
Copy
Edit
{
  "transcription": "I believe traveling is a great way to learn.",
  "mode": "Test",
  "part": 1
}
Response Example:
json
Copy
Edit
{
  "fluency_score": 7,
  "fluency_feedback": "Good flow but some hesitation.",
  "grammar_score": 8,
  "grammar_feedback": "Very few errors, good range of structures."
}
📌 Full API Documentation → http://localhost:8000/docs

🤔 Common Issues & Fixes
❌ Flutter app cannot connect to backend
Fix: Replace http://localhost:8000 with your Render backend URL.
❌ Google Speech API fails
Fix: Ensure GOOGLE_SPEECH_CREDENTIALS is correctly set.
📜 License
This project is licensed under the MIT License.

👥 Contributors
Your Name → Flutter Developer
Your Teammate → Backend Developer
📬 Contact
For support, please open an issue or email:
📧 your.email@example.com
🔗 GitHub Repository: https://github.com/yourusername/ielts-speaking-app




