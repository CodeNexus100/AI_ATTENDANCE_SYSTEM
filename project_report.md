# Project Report: SnapClass AI Attendance System

## 1. Introduction
**SnapClass** is a modern, AI-powered attendance management system built to eliminate the traditional, time-consuming roll-call process. By leveraging Facial Recognition and machine learning, SnapClass instantly marks attendance for an entire classroom from a single uploaded photo.

## 2. Key Features

### For Teachers
* **Class Management:** Easily create new classes and generate unique shareable join codes, including automatic QR code generation.
* **AI Face Attendance:** Upload one or more photos of the classroom. The AI automatically scans, detects, and marks present students in seconds.
* **Attendance Records:** Keep track of historical attendance logs securely.

### For Students
* **Face ID Login & Registration:** Students securely log in and register their initial face profile using their webcam directly in the app.
* **Auto-Enrollment:** Seamlessly enroll in classes using a teacher's unique join link or code.
* **Track Progress:** View enrolled subjects and track personal attendance records across all classes.

## 3. Technical Architecture
The system is built on a robust, modern technology stack:

* **Frontend & UI:** Developed using **Streamlit** for a responsive, fast, and interactive web interface.
* **Backend Database:** Powered by **Supabase (PostgreSQL)**, utilizing Row Level Security (RLS) to ensure data privacy and secure access controls.
* **Artificial Intelligence (AI):** 
    * Built using **dlib** and **face_recognition_models** for high-accuracy face detection and 128-dimensional facial embedding extraction.
    * Uses **scikit-learn** Support Vector Classifier (SVC) for matching detected faces against the enrolled student database.
* **Data Processing:** Utilizes **numpy** for rapid mathematical array operations and threshold matching, along with **Pillow** for image handling.

## 4. System Workflow
1. **Enrollment:** A student captures a selfie using the webcam. The system extracts a facial embedding and stores it securely in Supabase.
2. **Class Creation:** A teacher creates a subject, generating a join code.
3. **Student Joining:** Students use the code or scan the QR code to enroll in the specific subject.
4. **Attendance Marking:** The teacher uploads a classroom photo. The system detects all faces, extracts their embeddings, and runs them against the trained SVC model of enrolled students to mark attendance.

## 5. Conclusion
SnapClass successfully demonstrates the integration of advanced machine learning models into a user-friendly web application, providing an efficient, scalable, and secure solution for classroom attendance tracking.
