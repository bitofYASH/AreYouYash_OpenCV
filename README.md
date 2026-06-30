# 👤 Face Detection using OpenCV

A real-time face detection system built using OpenCV and Haar Cascade Classifier.  
This project captures live video from a webcam and detects human faces with bounding boxes and labels.

---

## 📌 Project Overview

This application:

- Uses OpenCV for computer vision
- Loads a pre-trained Haar Cascade model
- Captures real-time video from webcam
- Detects faces in each frame
- Draws bounding boxes around detected faces
- Displays "FACE DETECTED" label

---

## 🛠️ Technologies Used

- Python 3.x
- OpenCV (cv2)
- Haar Cascade Classifier (Viola-Jones Algorithm)

---

## 📂 Project Structure

```bash
Face-Detection/
├── face-reco.py
├── haarcascade_frontalface_default.xml
└── README.md
```

---

## 🚀 Getting Started

### 1️⃣ Prerequisites

Make sure you have:

- Python 3.x installed
- pip installed

---

### 2️⃣ Install Dependencies

```bash
pip install opencv-python
```

---

## ▶️ Run the Project

```bash
python face-reco.py
```

---

## 🎥 How It Works

1. Loads the Haar Cascade classifier for frontal face detection.
2. Opens the default webcam (device index 0).
3. Converts each frame to grayscale.
4. Detects faces using:

```python
detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5)
```

5. Draws a green rectangle around detected faces.
6. Displays "FACE DETECTED" below the face.
7. Press **ESC key** to exit.

---

## 🧠 Face Detection Method

This project uses:

**Haar Cascade Classifier**

- Based on the Viola-Jones object detection framework
- Fast and lightweight
- Suitable for real-time detection
- Works by detecting facial features at multiple scales

---

## ⌨️ Controls

| Key | Action |
|-----|--------|
| ESC | Exit the application |

---

## 🛑 Stopping the Application

Press:

```
ESC
```

The webcam will be released and all windows will close properly.

---

## 🎯 Features

- Real-time face detection
- Lightweight and fast
- Beginner-friendly implementation
- Clean and simple structure

---

## 🚀 Future Improvements

- Add face recognition
- Add multiple face tracking
- Add emotion detection
- Convert into a web application
- Deploy using Flask or Streamlit

---

## 📜 License

This project is open-source and free to use.

---

