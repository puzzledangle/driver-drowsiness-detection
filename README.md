# Driver Drowsiness Detection System

## Project Information
This project was developed as part of a **4th Semester Design Thinking and Innovation course project**.

### Team Members
- Alankrit Kasana
- Utkarsh Kumar
- Anany Dixit

B.Tech Computer Science Engineering

---

## Overview
This project implements a real-time driver drowsiness detection system using computer vision techniques. The system monitors the driver's eyes through a webcam and detects signs of fatigue using the Eye Aspect Ratio (EAR).

Facial landmarks are detected using the **dlib 68-point facial landmark predictor**. The Eye Aspect Ratio is calculated from the detected eye landmarks to determine whether the driver's eyes are open or closed. If the eyes remain closed for a predefined number of frames, the system triggers an alert sound to warn the driver.

The aim of the project is to demonstrate how computer vision can help improve road safety by detecting driver fatigue and warning the driver before an accident occurs.

---

## Project Status

This project is currently under development as part of our 4th semester coursework. The current version includes a working prototype that detects eye closure using the Eye Aspect Ratio (EAR) and triggers an alert when drowsiness is detected.

Future development will focus on improving detection accuracy, adding additional fatigue indicators, and improving the usability of the system.

---

## Features

- Real-time face detection
- Eye landmark detection using dlib
- Eye Aspect Ratio (EAR) calculation
- Detection of prolonged eye closure
- Alert sound when drowsiness is detected
- Real-time EAR value display
- FPS display for performance monitoring

---

## Technologies Used

- Python
- OpenCV
- dlib
- SciPy
- imutils
- NumPy

---

## How the System Works

1. The webcam captures live video frames.
2. Each frame is converted to grayscale for processing.
3. The dlib face detector identifies faces in the frame.
4. Facial landmarks are extracted using the 68-point landmark model.
5. Eye landmark points are isolated from the landmarks.
6. The Eye Aspect Ratio (EAR) is calculated.
7. If the EAR remains below a predefined threshold for several frames, the system identifies possible drowsiness.
8. An alert sound is triggered to warn the driver.

---

## Project Structure

```
driver-drowsiness-detection
│
├── main.py
├── README.md
├── requirements.txt
└── models
    └── shape_predictor_68_face_landmarks.dat
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/puzzledangle/driver-drowsiness-detection.git
```

Navigate into the project folder:

```bash
cd driver-drowsiness-detection
```

Install the required libraries:

```bash
pip install opencv-python dlib imutils scipy numpy
```

---

## Running the Project

Run the following command:

```bash
python main.py
```

Ensure that a webcam is connected and accessible.

Press **Q** to exit the program.

---

## Future Improvements

Possible future improvements include:

- Yawn detection
- Head pose estimation
- Deep learning based fatigue detection
- Mobile application integration
- Integration with vehicle safety systems

---

## Disclaimer

This system is intended as a driver assistance tool and may not always provide perfectly accurate results. Environmental conditions such as lighting, camera positioning, or facial obstruction may affect detection accuracy. Drivers remain responsible for safe driving at all times.
