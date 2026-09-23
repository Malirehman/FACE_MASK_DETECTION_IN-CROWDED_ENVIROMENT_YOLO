# 😷 Face Mask Detection in Crowded Environments Using YOLO

**A YOLO-based computer vision system for detecting faces and classifying them as Mask or No Mask in images, videos, and live webcam streams.**

---

## 📌 Overview

**Face Mask Detection in Crowded Environments Using YOLO** is a computer vision project developed as a Final Year Project for the **BS Computer Science** program.

The system uses a trained **YOLO object detection model** to detect multiple faces in a scene and classify each detected face into two categories:

- 😷 **Mask**
- ❌ **No Mask**

Unlike a traditional two-stage approach, where a separate face detector is followed by a classifier, the YOLO-based system performs detection and classification within a single detection pipeline.

The project is designed to work with:

- 📷 Images
- 🎥 Recorded videos
- 📹 Live webcam streams
- 👥 Crowded scenes

---

## 🎯 Project Objectives

1. **To develop a YOLO-based system** capable of detecting faces and classifying them as **Mask** or **No Mask**.

2. **To prepare and use YOLO-format annotated data** for training and testing the face mask detection model.

3. **To test the system under practical conditions**, including crowded scenes, side-facing faces, partial occlusion, blur, and low-quality or poorly illuminated frames.

4. **To implement a practical inference workflow** using the trained `best.pt` model, Python, and OpenCV, with clear bounding boxes, class labels, and confidence values.

---

## ✨ Features

### 🔍 Multi-Face Detection

Detects multiple faces within the same frame rather than processing only one person at a time.

### 😷 Mask / No Mask Classification

Each detected face is classified as:

`Mask` or `No Mask`

### 📦 Bounding Boxes

Detected faces are displayed using bounding boxes directly on the original frame.

### 📊 Confidence Scores

The system displays the model's confidence value alongside each prediction.

### 🎥 Video Processing

The trained model can process recorded video files frame by frame.

### 📹 Webcam Detection

The inference pipeline can be connected to a webcam for live detection.

### 🧠 YOLO-Based Detection

The project uses the YOLO detection framework through **Ultralytics**.

### 💻 Practical Deployment Workflow

Training is performed in a cloud notebook environment, while the trained model can be transferred to a local environment for inference.

---

## 🏗️ System Workflow

```text
Dataset Images
      │
      ▼
YOLO Annotation
(Mask / No Mask)
      │
      ▼
Model Training
(Google Colab)
      │
      ▼
best.pt
(Trained Model)
      │
      ▼
facemask.ipynb
(Inference)
      │
      ├──────────────┬──────────────┐
      ▼              ▼              ▼
   Images         Videos          Webcam
      │              │              │
      └──────────────┴──────────────┘
                     │
                     ▼
              YOLO Predictions
                     │
                     ▼
          Annotated Detection Output
          • Bounding Boxes
          • Mask / No Mask
          • Confidence Scores
