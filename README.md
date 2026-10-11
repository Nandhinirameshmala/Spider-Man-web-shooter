Spider-Man AR Experience Using Python
Overview

The Spider-Man AR Experience is a computer vision project that combines real-time face tracking, hand gesture recognition, and graphical effects to create an interactive Spider-Man-inspired experience using a webcam.

The application overlays a Spider-Man mask onto the user's face and detects a specific hand gesture to trigger a web-shooting animation. The web and impact effects are generated programmatically rather than relying on pre-made web animation images.

This project explores how computer vision and real-time graphics can be combined to create interactive Augmented Reality (AR) experiences.

Features
Real-Time Face Tracking: Detects facial landmarks and positions the Spider-Man mask according to the user's face.
AR Mask Overlay: Resizes, positions, and rotates the mask to follow facial movement.
Hand Tracking: Detects hand landmarks using MediaPipe.
Gesture Recognition: Recognizes a Spider-Man-inspired hand gesture to trigger the web-shooting effect.
Procedural Web Generation: Creates graphical web strands, connecting threads, curves, and glow effects using OpenCV.
Graphical Impact Effect: Generates a visual impact animation when the web reaches its target.
Live Webcam Processing: Combines tracking, gesture recognition, and graphical rendering in real time.
Technologies Used
Python
OpenCV
MediaPipe
NumPy
Computer Vision
Augmented Reality
Procedural Graphics
How It Works
1. Face Detection and Mask Placement

MediaPipe Face Mesh identifies facial landmarks. The application uses these landmarks to estimate face position, width, height, and orientation, allowing the mask overlay to follow the user's movements.

2. Hand Tracking

MediaPipe Hands detects the hand and tracks key points, including finger joints and fingertips.

3. Gesture Recognition

The application checks finger positions to recognize a predefined web-shooting gesture. When the gesture is detected, the web animation is triggered.

4. Web Animation

OpenCV draws the web dynamically using graphical strands and connecting lines. The animation moves from the hand toward the target area.

5. Impact Animation

When the web reaches its target, a procedural graphical effect is displayed to simulate the impact.

6. Real-Time Rendering

The face mask, hand tracking, gesture detection, and web effects are processed together in the webcam feed.

Project Structure
SpiderMan_Project/
├── main.py
└── assets/
    └── spiderman_mask.png

Note: The mask image is required. The web and impact effects are generated through code, so separate web animation PNG files are not required.

Requirements
Python 3.11 recommended
A working webcam
Windows, or another operating system supported by the required libraries
Installation
1. Clone the Repository
git clone https://github.com/YOUR-USERNAME/SpiderMan_Project.git
cd SpiderMan_Project

Replace YOUR-USERNAME with your GitHub username.

2. Create a Virtual Environment
python -m venv venv311

Activate it on Windows:

venv311\Scripts\activate
3. Install Dependencies
python -m pip install opencv-python mediapipe numpy

If your project uses OpenCV's additional modules, install opencv-contrib-python instead of installing both OpenCV packages.

4. Add the Mask Asset

Place your Spider-Man mask image in the assets folder and name it:

spiderman_mask.png

Make sure the image path in the Python code matches this filename.

5. Run the Project
python main.py

The webcam window should open and display the AR experience. Press Q to exit if the application uses q as its quit key.

Learning Outcomes

Through this project, I explored:

Facial landmark detection and tracking
Hand landmark detection and gesture recognition
Real-time image processing with OpenCV
Overlay positioning, resizing, and rotation
Programmatic generation of graphical effects
Integration of multiple computer vision components
Debugging camera access, asset paths, and real-time processing
Future Improvements

Potential enhancements include:

More accurate gesture recognition
Multiple web-shooting gestures
Improved web physics and animation
More realistic impact and crack effects
Additional AR masks and visual effects
Performance optimization for smoother real-time processing
Project Purpose

This project was developed as a hands-on exploration of computer vision, interactive graphics, and Augmented Reality. It demonstrates how Python can be used to transform a creative idea into a real-time interactive application.

Author

Nandhini Ramesh

Interested in Python, Computer Vision, Artificial Intelligence, Robotics, and interactive technology projects.

If you find this project interesting, feel free to explore the code and share suggestions for future improvements.
