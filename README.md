# Gesture Control System 👋🖱️

This Gesture Control System allows users to control various system functions (like mouse movement, volume adjustment, and screen brightness) using hand gestures through a webcam. It leverages **MediaPipe** for hand tracking and **PyAutoGUI** for controlling the system. The project enables intuitive, hands-free control for everyday tasks.

---

## 📋 Table of Contents

1. [Installation](#installation)
2. [How it Works](#how-it-works)
3. [Features](#features)
4. [Supported OS](#supported-os)
5. [Configuration](#configuration)
6. [Cloning (Optional)](#cloning-optional)
7. [Usage](#usage)
8. [Components / File Structure](#components-file-structure)
9. [Contributing](#contributing)
10. [License](#license)
11. [Acknowledgments](#acknowledgments)

---

## 🚀 Installation

### Prerequisites

- Python 3.8+ (preferably 3.9)
- Make sure you have **pip** installed for managing Python packages.

### Steps to Install

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/ArchitJ6/Gesture-Control-System.git
    cd Gesture-Control-System
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Additional packages for specific platforms:
   - **Windows**: Install Visual C++ Redistributable for Visual Studio.
   - **Linux/Mac**: Ensure `libopencv` and `libmediapipe` are installed.

---

## 🔧 How it Works

The system utilizes a webcam to track the user's hand gestures, which are interpreted to trigger different actions like mouse movements, clicks, and adjusting system volume/brightness.

- **Hand gestures** are captured in real-time using **MediaPipe**.
- The captured gestures are mapped to system controls using **PyAutoGUI** and **PyCaw**.
- This project runs the webcam feed, detecting hand gestures and interpreting them into actions.

---

## 🌟 Features

| Feature                       | Gesture Description                                                         |
|-------------------------------|------------------------------------------------------------------------------|
| **No Action Performed**        | When all five fingers are up, the cursor stops moving.                       |
| **Cursor Moving**              | When both the index and multiple fingers are raised, the cursor moves.       |
| **Left Button Click**          | Lower the index finger and raise the middle finger to perform a left-click.   |
| **Right Button Click**         | Lower the middle finger and raise the index finger to perform a right-click.  |
| **Brightness Control**         | Pinch with index and thumb, raise other fingers, and move hand horizontally. |
| **Volume Control**             | Pinch with index and thumb, raise other fingers, and move hand vertically.   |
| **Scrolling Vertically**       | With the left hand, pinch with index and thumb, raise other fingers, and move hand vertically. |
| **Drag & Drop**                | Lower all fingers after selecting an element, drag it, and drop it.          |
| **Double Click**               | Join/close index and middle fingers to perform a double-click action.        |

---

## 💻 Supported OS

| OS          | Supported |
|-------------|-----------|
| **Windows** | ✅ Yes     |
| **Linux**   | ✅ Yes     |
| **Mac**     | ✅ Yes     |

---

## 🔄 Cloning (Optional)

If you'd like to fork or clone this project for your own use, you can follow these steps:

1. Fork the repository on GitHub to your own account.
2. Clone your forked repository to your local machine:

    ```bash
    git clone https://github.com/ArchitJ6/Gesture-Control-System.git
    ```

3. Navigate to the project directory:

    ```bash
    cd Gesture-Control-System
    ```

---

## 📦 Usage

To start using the Gesture Control System, run the following command:

```bash
python main.py
```

- The webcam will launch and start detecting your hand gestures.
- The corresponding actions (mouse movement, clicks, etc.) will be triggered based on the gestures you make.

---

## 🗂️ Components / File Structure

```
gesture-control-system/
│
├── Constants.py           # Contains configuration constants
├── Controller.py          # Logic for system controls (mouse, volume, etc.)
├── GestureController.py   # Manages gesture classification and interpretation
├── HandRecog.py           # Hand recognition logic and gesture detection
├── main.py                # Main script to run the system
├── requirements.txt       # Required Python dependencies
└── README.md              # Project documentation
```

---

## 🤝 Contributing

We welcome contributions! If you'd like to help improve the system, feel free to follow these steps:

1. Fork the repository.
2. Clone your forked repository to your local machine:

    ```bash
    git clone https://github.com/ArchitJ6/Gesture-Control-System.git
    ```

3. Create a new branch for your changes:

    ```bash
    git checkout -b feature-branch
    ```

4. Make your changes and commit them:

    ```bash
    git commit -m "Add new feature XYZ"
    ```

5. Push your branch:

    ```bash
    git push origin feature-branch
    ```

6. Open a pull request and describe your changes.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 💡 Acknowledgments

- **MediaPipe**: For their hand tracking model.
- **PyAutoGUI**: For mouse control and automation.
- **PyCaw**: For controlling system volume on Windows.
- **OpenCV**: For real-time video capture and image processing.

---