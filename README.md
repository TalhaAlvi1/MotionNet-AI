# MotionNet-AI
<div align="center">
  <img src="https://img.shields.io/badge/MediaPipe-10.14.0-blue.svg" alt="MediaPipe Version">
  <img src="https://img.shields.io/badge/OpenCV-4.8.0-green.svg" alt="OpenCV Version">
  <img src="https://img.shields.io/badge/Python-3.8+-yellow.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License">
  <img src="https://img.shields.io/badge/Colab-Open%20Now-orange.svg?logo=google-colab" alt="Open In Colab">
</div>

<br>

<p align="center">
  <img src="https://raw.githubusercontent.com/yourusername/MotionNet-Video-Analyzer/main/assets/demo.gif" alt="MotionNet Demo" width="600">
</p>

<h1 align="center">🎯 MotionNet Video Analyzer</h1>

<h3 align="center">Real‑time Human Pose & Hand Tracking with Weapon‑Stance Detection</h3>

<p align="center">
  <em>Powered by MediaPipe • Built for Security & Motion Analysis</em>
</p>

---

## 📊 System Architecture

```mermaid
flowchart TD
    A[📹 Input Video] --> B[MediaPipe Pose]
    B --> C{Weapon Stance Detected?}
    C -->|❌ No| D[📝 Log Pose Only]
    C -->|✅ Yes| E[✋ MediaPipe Hands]
    E --> F[🎯 Log Event + Timestamp]
    D --> G[🎨 Overlay Visuals]
    F --> G
    G --> H[📤 Output Video + JSON]
    
    style A fill:#ff6b6b,stroke:#c92a2a,color:#fff
    style B fill:#4ecdc4,stroke:#0b5e5e,color:#fff
    style C fill:#ffe66d,stroke:#f59f00,color:#000
    style E fill:#4ecdc4,stroke:#0b5e5e,color:#fff
    style H fill:#a8e6cf,stroke:#2d8f6a,color:#000
