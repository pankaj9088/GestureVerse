# Celestial Particles

GestureVerse is a computer vision–based hand gesture recognition system that enables touchless control of computer functions using real-time hand movements captured through a webcam. Built with Python, OpenCV, and MediaPipe, it detects hand landmarks and converts gestures into actions such as mouse movement, clicking, and keyboard input, providing a natural and interactive human-computer interaction experience.

## Overview
This project combines **Three.js** for high-performance 3D graphics and **MediaPipe Hands** for real-time machine learning-based hand tracking. It creates a dynamic "Celestial" particle system that responds to your physical hand movements, allowing you to manipulate the particles in 3D space as if you were touching them.

## Features
- **Real-time Hand Tracking**: Uses Google's MediaPipe to detect 21 3D hand landmarks directly in the browser with high precision.
- **3D Particle System**: Renders 8,000 individual particles using Three.js points material.
- **Gesture Controls**:
    - **Rotate & Move**: Move your index finger to rotate the particle system on X/Y axes.
    - **Scale/Zoom**: Pinch or expand the distance between your thumb and index finger to scale the system size dynamically.
    - **Shape Morphing**: Show an open palm gesture to seamlessly morph the particles into different shapes (Sphere, Heart, Flower, Saturn, Fireworks).
- **Dynamic Visuals**:
    - Particles change color hue based on your hand's X-axis position.
    - Includes a debug overlay showing the camera feed and tracked hand skeleton.

## Usage
1. Open the file `planet.html`.
   - **Important**: Due to browser security restrictions on camera access and ES modules, you must serve this file over a local server (http/https protocol) rather than opening it directly from the file system (`file://`).
   - *Suggested tools*: Live Server extension for VS Code, `npx serve`, or `python -m http.server`.
2. Allow camera access when prompted by the browser.
3. Stand back slightly so your hand is clearly visible to the camera.
4. Interact:
   - **Rotate**: Move your hand around the screen.
   - **Scale**: Pinch your thumb and index finger together to shrink, or move them apart to expand.
   - **Change Shape**: Hold your hand open (fingers extended) to cycle to the next shape. (Has a 2-second cooldown).

## Technical Details
- **Libraries**:
    - [Three.js](https://threejs.org/) (v0.160.0)
    - [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)
- **Implementation**:
    - Uses a `BufferGeometry` for efficient particle rendering.
    - Custom shape generation logic maps particles to mathematical functions for each form.
    - Hand landmarks are mapped to 3D scene parameters (rotation, scale, color).



