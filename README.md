# Driver Drowsiness Detection System

## Overview

This project implements a real-time **Driver Drowsiness Detection System** using computer vision. The system monitors the driver’s eye movements through a webcam and detects drowsiness based on the **Eye Aspect Ratio (EAR)**. If the driver’s eyes remain closed for a prolonged period, an alarm is triggered to alert the driver.

---

## Features

* Real-time face detection using dlib
* Facial landmark detection (68-point model)
* Eye Aspect Ratio (EAR) calculation
* Drowsiness detection based on consecutive closed-eye frames
* Alarm alert using system sound

---

## Technologies Used

* Python
* [OpenCV](https://opencv.org/?utm_source=chatgpt.com)
* NumPy
* SciPy
* [dlib](https://dlib.net/?utm_source=chatgpt.com)
* imutils

---

## Working Principle

1. Capture video from webcam.
2. Detect face in each frame.
3. Predict 68 facial landmarks.
4. Extract left and right eye landmarks.
5. Compute Eye Aspect Ratio (EAR).
6. If EAR falls below threshold for multiple consecutive frames, detect drowsiness.
7. Trigger alarm sound.

---

## Eye Aspect Ratio Formula

EAR = (A + B) / (2 × C)

Where:

* A and B = vertical eye distances
* C = horizontal eye distance

If EAR becomes low, it indicates eye closure.

---

## Installation

Clone repository:

```bash
git clone <your_repo_link>
cd driver-drowsiness-detection
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Download landmark predictor:

* `shape_predictor_68_face_landmarks.dat`
* You can download it from Kaggle here:
  [shape-predictor-68-face-landmarks.dat](https://www.kaggle.com/datasets/sergiovirahonda/shape-predictor-68-face-landmarksdat)
* Place the `.dat` file in the project root folder

---

## Usage

Run:

```bash
python drowsiness_detection.py
```

Controls:

* Press **Q** to exit.

---

## Output

* Red contours are drawn around both eyes.
* When prolonged eye closure is detected:

  * Warning text appears
  * Alarm sound is played

---

## Future Improvements

* Yawn detection
* Head pose monitoring
* Mobile deployment
* Deep learning–based fatigue detection
* Integration with smart vehicle systems

---

## Applications

* Automotive safety systems
* Driver monitoring systems (ADAS)
* Fleet management
* Accident prevention

---

## Author

Harshini S — Robotics and Automation Engineering Student
