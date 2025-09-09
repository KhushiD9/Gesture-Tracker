# **Head Pose Controlled Servo Motor System**

## **📚 Project Description**

This project uses computer vision and embedded systems to control a servo motor based on the direction of a person’s face. By tracking head movements (pitch, yaw, roll) using a camera and facial landmarks, it adjusts the servo motor in real time to reflect the user’s head orientation. It is useful in applications such as assistive technologies, human-computer interaction, and robotics.

---

## **🚀 Key Features**

- Real-time head pose estimation using OpenCV and dlib.
- Face detection with 68-point landmark predictor.
- Pitch, Yaw, and Roll angles calculated using solvePnP.
- Servo motor control via Arduino based on yaw angle.
- Data logging of head pose (pitch, yaw, roll) to CSV for analysis.
- Visual feedback of head orientation overlaid on camera feed.
- User-friendly: Press 'q' to quit the program safely.

---

## **🔧 Components**

- **Arduino UNO** – Controls the servo motor.
- **Servo Motor** – Rotates according to the user’s head yaw.
- **Computer (with Python environment)** – Runs OpenCV and dlib for head tracking.
- **Webcam** – Captures live video for real-time processing.
- **Dlib Shape Predictor** – Pre-trained model for detecting facial landmarks (`shape_predictor_68_face_landmarks.dat`).
- **Serial Communication** – Communicates head pose angles to Arduino.
- **Power Supply** – Powers Arduino and servo.

---

## **⚙️ How It Works**

1. The webcam continuously captures video frames.
2. Dlib’s face detector identifies faces and predicts 68 facial landmarks.
3. The system estimates the head pose by calculating pitch, yaw, and roll from landmark positions.
4. The yaw value is mapped to a servo angle (0° to 180°).
5. The angle is sent via serial communication to the Arduino, which drives the servo accordingly.
6. Head pose data is stored in a CSV file for further analysis.

---

## **📊 Data Output**

The system stores real-time pitch, yaw, and roll values into a CSV file:
```text
head_posture_data.csv
