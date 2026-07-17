# Screen Recorder 🎥

A simple and lightweight screen recording script written in Python using OpenCV, PyAutoGUI, and NumPy. It captures the screen at a specified frame rate and saves it as an MP4 video file.

*Developed by [Ariful Islam](https://github.com/Ariful-Islam010)*

---

## 🚀 Features

- **Full Screen Recording:** Automatically detects system screen resolution and records the full screen.
- **Customizable Duration:** Easily set the recording duration (defaults to 14 seconds).
- **High Performance:** Uses `numpy` and `pyautogui` for fast frame capturing.
- **Standard Video Output:** Saves the recording in `test.mp4` using the `XVID` video codec.

---

## 🛠️ Prerequisites & Installation

To run this project, you need to install the required Python libraries. You can install them by running:

```bash
pip install opencv-python pyautogui numpy pywin32
```

> [!NOTE]
> The `pywin32` package is required on Windows to dynamically fetch screen resolution metrics.

---

## 💻 How to Use

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/Ariful-Islam010/screen_recoder.git
   cd screen_recoder
   ```
2. Run the script:
   ```bash
   python sc_recoder.py
   ```
3. Once completed, you will see `--Done--` printed in the terminal, and a `test.mp4` file will be generated in the same directory.

---

## ⚙️ Configuration & How it Works

The script performs the following steps:
1. Retrieves screen dimensions using `win32api.GetSystemMetrics`.
2. Initializes OpenCV's `VideoWriter` with the `XVID` codec.
3. Loops for the specified duration (default is 14 seconds, configured by the `dur` variable in `sc_recoder.py`).
4. Captures screenshots using `pyautogui.screenshot()`.
5. Converts each captured image from BGR to RGB color space.
6. Writes each frame to the video file.
7. Releases resources and saves the final file.
