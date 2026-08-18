---
layout: page
title: Sentinel AI — Computer Vision Security System
description: Real-time AI security system detecting weapons, suspicious behavior, and robbery gestures using YOLOv8, MediaPipe, Flask, MySQL, and Twilio WhatsApp alerts.
img: assets/img/12.jpg
importance: 1
category: Artificial Intelligence & Computer Vision
giscus_comments: false
---

## Overview

**Sentinel AI** is a real-time computer-vision security and threat-detection platform designed for instant automated detection and emergency response. It leverages state-of-the-art deep learning models (**YOLOv8** and **MediaPipe**) to detect concealed/visible weapons, suspicious behavioral patterns, and robbery gestures from live video streams.

---

## Key Features

- **Real-Time Threat Detection**: Leverages **YOLOv8** object detection and **MediaPipe** pose estimation for immediate identification of weapons, aggressive movements, and robbery gestures.
- **Role-Based Incident Dashboard**: Developed a web dashboard using **Flask** and **MySQL** for managing civilian reports, incident logs, and law-enforcement access levels.
- **Automated Multi-Channel Alerting**: Integrated **Twilio API** to dispatch real-time WhatsApp emergency alerts with captured evidence photos and threat-location routing to responders.

---

## Tech Stack & Architecture

- **AI & Computer Vision**: Python, YOLOv8, MediaPipe, OpenCV, PyTorch
- **Backend & Web**: Flask, MySQL, REST API
- **Alerting & Communications**: Twilio API (WhatsApp Notifications & Incident Media Routing)
- **Database & Tools**: MySQL, XAMPP, Git, Linux
