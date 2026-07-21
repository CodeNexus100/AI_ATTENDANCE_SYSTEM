<div align="center">
  <img src="https://i.ibb.co/YTYGn5qV/logo.png" alt="SnapClass Logo" width="150" />
  <h1>SnapClass</h1>
  <p><em>Making Attendance Faster Using AI</em></p>
</div>

---

## 📖 Overview

**SnapClass** is a modern, AI-powered attendance management system built with Python, Streamlit, and Supabase. It eliminates the traditional roll-call process by leveraging **Facial Recognition** to instantly mark attendance for an entire classroom from a single photo!

Whether you are a teacher looking to save time or a student looking for a seamless check-in experience, SnapClass has you covered.

## ✨ Key Features

### 🧑‍🏫 For Teachers
- **Create & Manage Subjects:** Easily create new classes and generate unique shareable join codes (QR code support included).
- **AI Face Attendance:** Upload one or more photos of your classroom, and the AI will automatically scan and mark present students in seconds!
- **Attendance Records:** Keep track of historical attendance logs and export them as needed.

### 🎓 For Students
- **Face ID Login & Registration:** Students securely log in and register their initial face profile using their webcam.
- **Auto-Enrollment:** Seamlessly enroll in classes using a teacher's unique join link or code.
- **Track Progress:** View your enrolled subjects and track your attendance record across all classes.

---

## 🛠️ Tech Stack

- **Frontend / UI:** [Streamlit](https://streamlit.io/)
- **Backend / Database:** [Supabase](https://supabase.com/) (PostgreSQL)
- **AI / Machine Learning:** `dlib`, `face_recognition`, `scikit-learn`
- **Other Utilities:** `pandas`, `numpy`, `pillow`, `segno` (for QR codes), `bcrypt`

---

## 🚀 Getting Started

Follow these instructions to set up the project locally on your machine.

### 1. Prerequisites
- Python 3.10 or higher
- A free [Supabase](https://supabase.com/) account

### 2. Installation
Clone the repository and install the dependencies. We highly recommend using a virtual environment!

```bash
# Create and activate a virtual environment
python -m venv venv
.\venv\Scripts\activate   # On Windows
# source venv/bin/activate # On Mac/Linux

# Install all required packages
pip install -r requirements.txt
```

> **Note for Windows users:** If you face issues installing `dlib`, make sure you install the pre-compiled version provided in the requirements (`dlib-bin`).

### 3. Database Setup (Supabase)
1. Create a new project on Supabase.
2. Go to the **SQL Editor** in your Supabase dashboard.
3. Copy the contents of the `schema.sql` file (located in the root of this repository) and run it to create the necessary tables (`teachers`, `students`, `subjects`, `subject_students`, `attendance_logs`).

### 4. Configure Secrets
Streamlit uses a `secrets.toml` file to securely connect to your database. 
1. Inside the project folder, create a `.streamlit` folder.
2. Inside `.streamlit`, create a file named `secrets.toml`.
3. Add your Supabase credentials like this:

```toml
SUPABASE_URL = "https://your-project-id.supabase.co"
SUPABASE_KEY = "sb_publishable_your_api_key_here"
```
*(You can find these in your Supabase Dashboard under Settings > API)*

### 5. Run the App
Start the Streamlit server:
```bash
python -m streamlit run app.py
```
The app will open automatically in your browser at `http://localhost:8501`.

Streamlit Deployed Link : https://snapclass-app-ai.streamlit.app

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

---
