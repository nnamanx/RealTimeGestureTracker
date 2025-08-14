# REAL TIME GESTURE TRACKER

*Transforming Gestures into Instant Interactive Power*

![Last Commit](https://img.shields.io/github/last-commit/nnamanx/RealTimeGestureTracker?color=grey&label=last%20commit)
![GitHub Activity](https://img.shields.io/github/commit-activity/w/nnamanx/RealTimeGestureTracker)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Languages](https://img.shields.io/github/languages/count/nnamanx/RealTimeGestureTracker)

---

*Built with the tools and technologies:*

<!-- Tech Stack -->
![Python](https://img.shields.io/badge/Python-3.11-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-blueviolet)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0.10-orange)


---

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Testing](#testing)

---

## Overview
<p> Real-time hand gesture recognition project using Python, OpenCV, and MediaPipe. Currently in early development — features will be improved and more gestures will be added. </p>
---

### Notes
<p>min_detection_confidence = 0.7</p>
<ul>
  <li>If confidence drops below <strong>0.5</strong>, MediaPipe will stop tracking that hand until it’s detected again.</li>
  <li><span style="color:green;">Higher values (e.g., 0.8)</span> → more accuracy, but the hand may “disappear” more often if detection isn’t strong.</li>
  <li><span style="color:orange;">Lower values (e.g., 0.3)</span> → more tolerant, but increases the chance of false positives or “ghost” hands.</li>
</ul>

<h2>multi_hand_landmarks</h2>
<p>Contains all the hands it found. Since we only allow 1 hand, this will have <strong>0 or 1</strong>.</p>

<h2>How MediaPipe Hand Landmarks Work</h2>
<p>MediaPipe gives us 21 points per hand, each with:</p>
<ul>
  <li><code>x</code> = horizontal position (0 = left, 1 = right)</li>
  <li><code>y</code> = vertical position (0 = top, 1 = bottom)</li>
  <li><code>z</code> = depth (not important for this part)</li>
</ul>

<p>The points are numbered in a fixed order:</p>
<table border="1" cellpadding="5" style="border-collapse:collapse;">
  <tr>
    <th>Finger</th>
    <th>Indices</th>
    <th>Tip</th>
  </tr>
  <tr><td>Thumb</td><td>[1, 2, 3, 4]</td><td>4</td></tr>
  <tr><td>Index</td><td>[5, 6, 7, 8]</td><td>8</td></tr>
  <tr><td>Middle</td><td>[9, 10, 11, 12]</td><td>12</td></tr>
  <tr><td>Ring</td><td>[13, 14, 15, 16]</td><td>16</td></tr>
  <tr><td>Pinky</td><td>[17, 18, 19, 20]</td><td>20</td></tr>
</table>

<p><img src="img.ppm.png" alt="MediaPipe Hand Landmarks" style="max-width:100%;border:1px solid #ccc;border-radius:4px;"></p>
