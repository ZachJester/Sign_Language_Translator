
# Hand Gesture Recognition using MediaPipe

This is a lightweight real-time hand gesture recognition application built with Python. It uses **MediaPipe** for hand landmark detection and **OpenCV** for video capture and display. The app recognizes a few basic gestures (A, B, C) using geometric analysis of the hand landmarks.

## ✨ Features

- Real-time webcam-based hand tracking.
- Uses MediaPipe for robust hand landmark detection.
- Recognizes simple static gestures:
  - ✊ **A** – All fingers folded
  - 🖐️ **B** – All fingers extended
  - 🤜 **C** – Thumb farther from index than pinky
- Dual display:
  - Main video feed with annotated hand landmarks and gesture label.
  - Secondary window showing **landmark-only output** on a black canvas.

## 📂 File Structure

- `app.py` – Main GUI logic using Tkinter; handles video feed and gesture updates.
- `hand_tracking.py` – Gesture recognition logic using MediaPipe and hand landmark heuristics.

## 🧰 Requirements

- Python 3.7+
- [OpenCV](https://pypi.org/project/opencv-python/)
- [MediaPipe](https://pypi.org/project/mediapipe/)
- [Pillow (PIL)](https://pypi.org/project/Pillow/)
- [NumPy](https://pypi.org/project/numpy/)

## 🛠️ Installation

1. Clone this repository or copy the files locally.

2. Install the required Python packages:
   ```bash
   pip install opencv-python mediapipe pillow numpy


## ▶️ How to Run

Run the application from your terminal or command prompt:

```bash
python app.py
```

Make sure your webcam is connected and not used by other applications.

## 🧠 How Gesture Recognition Works

* **MediaPipe** detects 21 hand landmarks.
* Based on relative positions of key landmarks:

  * If all fingers are folded → "A"
  * If all fingers are extended → "B"
  * If thumb is curved away → "C"
* These conditions are implemented in the `recognize_gesture` method of `hand_tracking.py`.

## 📌 Notes

* Recognition is limited to static hand poses for letters A, B, and C.
* You can expand the system by adding more heuristics for other letters.
* This app does **not** use any trained machine learning model – it relies entirely on hand geometry.



## 📄 License

This project is open-source and free to use under the MIT License.

```
```
