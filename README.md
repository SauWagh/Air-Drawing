# Air Drawing Physics

A real-time computer vision application that lets you **draw in the air using hand gestures** and interact with your drawings using a realistic **2D physics engine**.

Instead of using a mouse or touchscreen, you simply move your hands in front of a webcam. The application recognizes your hand gestures using MediaPipe and turns them into drawing, erasing, object manipulation, and physics interactions.

---

# Features

## Air Drawing

* Draw in the air using your index finger.
* Drawing follows your fingertip with high accuracy.
* No mirrored drawing (your hand moves naturally).
* Smooth brush strokes.
* Adjustable pen thickness using pinch gesture.
* Multiple drawing colors.
* Real-time cursor.

---

## Eraser

* Erase drawings using a fist gesture.
* Circular eraser with smooth removal.
* Works naturally without changing tools.

---

## Physics Engine

After drawing, your sketches become physics objects.

Features include:

* Gravity
* Collision detection
* Bouncing
* Friction
* Rotation
* Velocity-based throwing
* Object stacking

Built using **Pymunk**.

---

# 🖐️ Right Hand Controls

| Gesture                | Action                       |
| ---------------------- | ---------------------------- |
| ☝️ Index Up            | Draw                         |
| 🤏 Thumb + Index Pinch | Change Brush Size            |
| ✊ Fist                 | Erase                        |
| 🖐️ Open Palm (Hold)   | Launch Drawings into Physics |

---

# 🤚 Left Hand Controls

| Gesture                  | Action               |
| ------------------------ | -------------------- |
| ✌️ Index + Middle Finger | Grab Physics Objects |
| ✊ Fist                   | Push Nearby Objects  |
| 🖐️ Open Palm            | Explosion Blast      |

---

# Finger UI (No Keyboard Required)

Everything can be controlled using hand gestures.

### Color Palette

Hover over a color for 0.5 seconds to select it.

### Toolbar

Hover over toolbar buttons to activate them.

### Radial Menu

Hold your right hand open for one second to open the radial menu.

No mouse is required.

---

# Keyboard Shortcuts

| Key     | Action                          |
| ------- | ------------------------------- |
| Space   | Launch Drawings                 |
| C       | Clear Canvas                    |
| Z       | Undo                            |
| G       | Toggle Gravity                  |
| T       | Toggle Motion Trails            |
| E       | Explosion                       |
| S       | Save Screenshot                 |
| + / -   | Increase or Decrease Brush Size |
| 1–8     | Change Drawing Color            |
| Q / ESC | Quit                            |

---

# How It Works

The application combines multiple technologies:

* OpenCV captures webcam frames.
* MediaPipe detects hand landmarks.
* Gesture recognition identifies different hand poses.
* Pygame renders the interface.
* Pymunk simulates realistic physics.
* NumPy performs mathematical calculations.

The complete pipeline runs in real time, creating a smooth interactive experience.

---

# Zero Mirror Drawing

Unlike many webcam drawing applications, this project **does not mirror the camera**.

The webcam image is processed exactly as captured.

Hand landmark coordinates are mapped directly to screen coordinates:

```
display_x = landmark.x × window_width
display_y = landmark.y × window_height
```

Because both the camera image and drawing canvas use the same coordinate system:

* Right hand moves right.
* Left hand moves left.
* Letters appear exactly as drawn.
* No reversed or mirrored writing.

This makes drawing feel much more natural.

---

# Technologies Used

* Python
* OpenCV
* MediaPipe
* Pygame
* Pymunk
* NumPy

---

# Installation

Clone the repository

```bash
git clone https://github.com/SauWagh/Air-Drawing.git
```

Go into the project folder

```bash
cd Air-Drawing
```

Install dependencies

```bash
pip install opencv-python mediapipe pymunk pygame numpy
```

Run the project

```bash
python main.py
```

---

# Project Highlights

* Real-time hand tracking
* Gesture recognition
* Air drawing
* Physics simulation
* Object grabbing
* Object throwing
* Explosion effects
* Brush resizing
* Multi-color drawing
* Motion trails
* Undo support
* Screenshot capture
* Zero mirror coordinate system
* Fully interactive finger-based UI

---

# Latest Feature Updates (v10)

✅ Two-hand gesture recognition

✅ Zero-mirror drawing system

✅ Real-time brush resizing

✅ Finger-controlled color selection

✅ Finger-controlled toolbar

✅ Physics-based drawing launch

✅ Velocity-based object throwing

✅ Grab and move physics objects

✅ Push nearby objects

✅ Area explosion effect

✅ Gravity toggle

✅ Motion trail effects

✅ Undo functionality

✅ Screenshot capture

✅ Improved drawing accuracy

✅ Faster gesture detection

✅ Smoother brush rendering

✅ Better collision handling

✅ More stable physics simulation

---

# Future Improvements

* Shape recognition
* AI gesture customization
* Multi-user support
* 3D physics
* More brush styles
* Drawing layers
* Save and load drawings
* Object scaling
* Voice commands
* Touchscreen support
* Custom gesture training
* Better UI animations

---

# Best Experience

* Good lighting
* Plain background
* Webcam positioned at eye level
* Keep both hands inside the camera frame
* Maintain a distance of about 50–80 cm from the camera

---

# Author

**Saurabh Waghamare**

Passionate about Computer Vision, AI, Full Stack Development, and building interactive applications using Python.

---
# 📦 Installation Guide

## 1. Clone the Repository

```bash
git clone https://github.com/SauWagh/Air-Drawing.git
```

## 2. Go to the Project Folder

```bash
cd Air-Drawing
```

---

# Create a Virtual Environment (Recommended)

### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

# Install Required Libraries

```bash
pip install opencv-python mediapipe pygame pymunk numpy
```

Or install everything using:

```bash
pip install -r requirements.txt
```

---

# Verify Installation

```bash
python -c "import cv2, mediapipe, pygame, pymunk, numpy; print('Everything Installed Successfully!')"
```

Expected output:

```
Everything Installed Successfully!
```

---

# Run the Project

```bash
python main.py
```

If your main file has another name, replace `main.py` with it.

Example:

```bash
python air_drawing.py
```

---

# Python Version

Recommended:

- Python 3.10
- Python 3.11

Python 3.12 also works for most setups.

Check your version:

```bash
python --version
```

---

# Required Packages

| Package | Purpose |
|----------|----------|
| OpenCV | Webcam input and image processing |
| MediaPipe | Hand tracking and gesture detection |
| Pygame | Window rendering and graphics |
| Pymunk | 2D Physics engine |
| NumPy | Mathematical calculations |

---

# requirements.txt

Create a file named **requirements.txt**

```
opencv-python
mediapipe
pygame
pymunk
numpy
```

Install everything:

```bash
pip install -r requirements.txt
```

---

# Camera Permission

Make sure your webcam is enabled.

### Windows

Settings → Privacy & Security → Camera

Enable:

- Camera Access
- Let desktop apps access your camera

---

# Common Errors

## ModuleNotFoundError

Install missing packages:

```bash
pip install -r requirements.txt
```

---

## Camera Not Opening

Close:

- Zoom
- Teams
- OBS
- Discord
- Any other application using the webcam

Then restart the project.

---

## Black Screen

- Check webcam permissions.
- Verify the correct camera index.
- Ensure your webcam is connected.

---

## MediaPipe Errors

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

Then reinstall:

```bash
pip install mediapipe
```

---

## Slow Performance

- Close unnecessary applications.
- Reduce camera resolution if supported.
- Ensure good lighting for faster hand detection.

---

# Recommended Hardware

- Webcam: 720p or 1080p
- CPU: Intel i5 / AMD Ryzen 5 or better
- RAM: 8 GB or more
- Operating System:
  - Windows 10/11
  - Ubuntu 22.04+
  - macOS 12+

---

# Tested On

- Windows 11
- Python 3.11
- OpenCV 4.x
- MediaPipe Latest
- Pygame 2.x
- Pymunk 7.x

---

# Tips for Best Experience

- Use good lighting.
- Keep your hands fully visible.
- Avoid cluttered backgrounds.
- Stay about 50–80 cm from the webcam.
- Keep the camera stable.

---
  
# Support

If you found this project useful:

Star this repository

Fork the project

Report issues

Suggest new features

Contributions are always welcome!
