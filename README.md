# Touchless Media Player 🎥✋

## 📌 Project Overview
The **Motion-Activated Media Player** is a computer vision-based application that enables users to control media playback using hand gestures. By leveraging real-time video input from a webcam, this project identifies and interprets hand gestures to perform common media actions like play, pause, forward, and rewind. This enhances user convenience and promotes a touchless, intuitive interaction with media content.

---

## 🚀 Objectives
- Develop a touchless media control system using computer vision and gesture recognition.
- Enable intuitive control of media playback through real-time hand gestures.
- Enhance user experience by making media interaction more natural and accessible.

---

## 🧠 Working Principle

1. **Video Capture**: Uses a webcam to capture real-time video.
2. **Hand Tracking**: Detects and tracks hand landmarks using MediaPipe.
3. **Gesture Recognition**: Interprets specific hand gestures by analyzing landmark positions.
4. **Media Control**: Converts recognized gestures into keyboard inputs using PyAutoGUI to control media playback.

---

## 🧱 Physical Design
- **Programming Language**: Python
- **Libraries Used**:
  - `OpenCV`: For video capture and image processing.
  - `MediaPipe`: For hand detection and tracking.
  - `PyAutoGUI`: For simulating media control key presses.
  - `Time`: For time management and delays.

---

## 🔧 Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/motion-media-player.git
   cd motion-media-player
````

2. Install dependencies:

   ```bash
   pip install opencv-python mediapipe pyautogui
   ```

3. Run the program:

   ```bash
   python main.py
   ```

---

## 🧩 Key Components & Functions

### 1. Libraries and Modules

* `cv2`: OpenCV for video and image processing.
* `mediapipe.solutions.hands`: For hand tracking.
* `mediapipe.solutions.drawing_utils`: To visualize hand landmarks.
* `pyautogui`: For media control via keyboard input.
* `time`: For delays and timing operations.

### 2. Important Functions

| Function                                    | Description                                                         |
| ------------------------------------------- | ------------------------------------------------------------------- |
| `cv2.VideoCapture(0)`                       | Captures video from the default webcam.                             |
| `cv2.flip(frame, 1)`                        | Horizontally flips the frame (mirror effect).                       |
| `cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)`    | Converts image color from BGR to RGB.                               |
| `hand_obj.process(frame)`                   | Detects hand landmarks in the frame using MediaPipe.                |
| `count_fingers(lst)`                        | Custom function to count extended fingers using landmark positions. |
| `pyautogui.press("right")`                  | Simulates pressing the "right arrow" key for media control.         |
| `drawing.draw_landmarks(...)`               | Draws hand landmarks and connections on the video frame.            |
| `cv2.imshow(...)`                           | Displays the video feed with annotations.                           |
| `cv2.waitKey(1)`                            | Waits for a key event; `ESC` to exit.                               |
| `cap.release()` / `cv2.destroyAllWindows()` | Frees resources and closes windows.                                 |

---

## 🔍 Feasibility Study

### 1. Economic Feasibility

* Utilizes standard webcams and open-source Python libraries.
* No special hardware or paid software required.

### 2. Operational Feasibility

* Simple and intuitive interface.
* No technical background needed to operate.

### 3. Behavioral Feasibility

* Tested with real users to evaluate usability and acceptance.

---

## 🎯 Scope

* Controls basic media playback operations: play, pause, forward, rewind.
* Compatible with common devices (webcams, PCs).
* Gesture recognition can be expanded to support more commands.

---

## 🧪 Testing & Evaluation

### Test Cases

* Performed different gestures under varying conditions.
* Validated whether gestures triggered the correct media actions.

### Performance Metrics

* **Accuracy**: Correct gesture recognition rate.
* **Responsiveness**: Time taken to respond to gestures.
* **Robustness**: Performance under different lighting and background scenarios.

---

## ⚠️ Limitations

* Currently supports a **limited set of gestures**.
* **Adequate lighting** is necessary for reliable hand tracking.
* Performance may vary based on webcam quality and environmental noise.

---

## 🔮 Potential Improvements

* Expand gesture library for more advanced controls.
* Improve robustness in varying lighting conditions.
* Optimize performance for real-time use on lower-end systems.
* Add support for dynamic gestures and gesture customization.

---

## 🧠 Computer Vision Techniques Used

* Background Subtraction (implicitly handled by MediaPipe).
* Hand Detection and Tracking (via MediaPipe).
* Gesture Recognition using landmark positions.

> Expression like `lst.landmark[5].y * 100 - lst.landmark[8].y * 100` computes vertical distances between landmarks, crucial for determining gesture posture (e.g., finger open or closed).

---

## 📚 References

* [OpenCV Documentation](https://docs.opencv.org/)
* [MediaPipe by Google](https://mediapipe.dev/)
* [PyAutoGUI Documentation](https://pyautogui.readthedocs.io/)

---

## 👨‍💻 Author

**Shubham Verma**
Project for Invertis University
https://www.linkedin.com/in/shubhver/

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
