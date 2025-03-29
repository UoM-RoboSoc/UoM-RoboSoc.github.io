---
title: Mona Delivery Bot
parent: 🧑‍💻 Tasks
layout: default
nav_order: 2
---

# Mona Delivery Bot

Welcome to the Mona Delivery Bot challenge! In this task, your objective is to program your provided Mona Bot to navigate a single-line maze and perform simulated payload pickups and dropoffs at designated points. Using a live video feed and computer vision, you must ensure that your bot stays on track and pauses at each checkpoint for the required duration. Read on for detailed information on maze and marker specifications, camera setup, communication protocols, scoring breakdown, testing guidelines, and more to help you succeed in this challenge.

![Maze]({{ '/assets/images/mona/maze.png' | relative_url }})

---

## Maze & Marker Specs

- **Marker Size & Shape**  
  The maze uses **fiducial markers** for the start, pickup, and dropoff points.  
  Fiducial markers are specially designed, high-contrast visual patterns (like QR codes) that are easy for a computer vision system to recognize and track.  
  Each marker will also be surrounded by a **color-coded border** to help spectators and teams visually identify them:
  - **Blue** for Start
  - **Red** for Pickup
  - **Green** for Dropoff

- **Line Width**  
  The path your Mona Bot must follow is marked using **standard electrical tape**, which is approximately **18mm wide** (though slight variations may occur). Make sure your line-following sensors are well-calibrated for this width.

- **Sample Images**  
  The images below show the actual markers placed on the maze to give you a visual reference for testing and training your computer vision system.

<div style="display: flex; justify-content: space-around; align-items: center; margin-top: 1em;">
  <figure style="text-align: center;">
    <img src="{{ '/assets/images/mona/start-marker.png' | relative_url }}" width="150" height="150" style="object-fit: cover;" />
    <figcaption>Start Marker</figcaption>
  </figure>
  <figure style="text-align: center;">
    <img src="{{ '/assets/images/mona/pickup-marker.png' | relative_url }}" width="150" height="150" style="object-fit: cover;" />
    <figcaption>Pickup Marker</figcaption>
  </figure>
  <figure style="text-align: center;">
    <img src="{{ '/assets/images/mona/dropoff-marker.png' | relative_url }}" width="150" height="150" style="object-fit: cover;" />
    <figcaption>Dropoff Marker</figcaption>
  </figure>
</div>

---

## Camera Setup & Streaming Details

- **Latency Considerations**  
  The overhead camera stream will be hosted via a **Raspberry Pi** (or laptop) connected directly to the **University of Manchester network**, ideally via **Ethernet** for minimal latency.  
  The stream will run at **720p resolution** with a **moderate framerate** to balance clarity and bandwidth—your code should be tolerant of occasional dropped frames or slight delays in the feed.

- **Resolution & Lighting**  
  The stream resolution is fixed at **1280x720 (720p)**.  
  While we aim for consistent and even lighting across the maze, **we cannot guarantee uniform conditions** throughout the event. Your computer vision solution should ideally include some form of adaptive thresholding or robustness to varied brightness levels.

- **Configuration Steps**  
  You’ll be provided with a **template Python script** that uses **OpenCV** to access the live video stream.  
  Competitors can either **fork the GitHub repository** or **download the ZIP** and build on the template code.  
  Further details (including usage instructions, stream URL, and example marker detection code) are provided in the **Resources & References** section later on this page.

---

## NRF / Communication Guide

- **Pairing Instructions**  
  Each Mona Bot comes with an **Arduino Nano** and an **NRF24L01 wireless communication module**, allowing your laptop to send and receive data to the bot.  
  You'll need to set up a corresponding **NRF module on your own laptop**, connected via USB, to serve as a wireless bridge between your control script and the robot.

  For hardware setup, code structure, and examples of communication protocols, refer to the official [ESP-MONA GitHub Repository](https://github.com/ICE9-Robotics).  
  This repo contains everything you need to get started with the **Mona Swarm platform**, including setup guidance for both **hardware and software**.

- **Command Protocol**  
  While you’re free to define your own control commands and packet structure, most teams will want to:
  - Send **direction and speed commands** from their vision code
  - Use **simple, low-latency packets** (e.g., forward/backward, left/right)
  - Optionally receive basic telemetry back (e.g., signal strength, confirmation)

  Example command structures and NRF setup guidance can also be found in the [ICE9-Robotics repo](https://github.com/ICE9-Robotics).

- **Manual vs. Autonomous**  
  Your system must be **fully autonomous once the run starts**.  
  During development, you’ll use your laptop to:
  - Run the **computer vision system**
  - Interface with the live **video stream**
  - **Send control commands** to the Mona Bot

  However, once the robot begins its run, **no interaction with the laptop is allowed**. The vision system and wireless control should operate without any further input from you or your team.

## Scoring Breakdown

- **Time Limits**  
  *5 minutes per run.*

---

## Testing & Practice

- **Location & Availability**  
  The Mona Bot maze will be available for **practice throughout the entire hackathon**. Students are encouraged to use any free time to test their code and calibrate their vision systems.

- **Backup Maze**  
  There is **no backup or secondary maze** available. Please treat the main maze with care — **do not damage or tamper with the layout**. It is the only one we’ll be using for both practice and judging.

- **Limitations**  
  At the start of the event, practice will be **first-come, first-served**. If things get too crowded or unmanageable, we may introduce a **queue system** later in the day to ensure fairness.

  During the judging phase, **final run times and queue order** will be announced separately.

---

## Final Demo

- **Number of Attempts**  
  Each team will have **a single official run** to complete the task. **No do-overs** will be allowed — if your robot fails to perform during the run, it will **not earn any points** for that cycle.

- **Mid-Run Adjustments**  
  Once your run begins, **you may not interact with the robot or your laptop**.  
  If your robot breaks or fails mid-run, **you cannot repair or adjust hardware** on the arena floor. Make sure everything is tested and reliable beforehand.

- **Judging Format**  
  The standard format is a **live demonstration** in which your bot must follow the maze autonomously.  
  However, if your robot struggles with line following, you may opt for a **reduced-score format**:  
  - Navigate from marker to marker (Start → Pickup → Dropoff) **without following the lines**, still using autonomous control.  
  - This will score **fewer points** but still demonstrates your system’s logic and vision capabilities.

---

## Equipment & Environment

- **Robot Specs**  
  The Mona Bot is a small wheeled platform designed for autonomous navigation and wireless control.  
  A picture of the standard Mona Bot build will be added here shortly, along with hardware notes.

  👉 [View the ICE9 Mona Bot GitHub Repository](https://github.com/ICE9-Robotics)  
  This contains full schematics, 3D-printed part files, wiring diagrams, and communication code for the Mona Swarm platform used in this challenge.

  ![Mona Bot]({{ '/assets/images/mona/mona-bot.png' | relative_url }}){: style="max-height: 200px;" }

- **Floor Material**  
  The maze will be built directly onto the floor of the **Nancy Rothwell Building** (previously known as MECD), using black electrical tape.

  ![Engineering Building Floor]({{ '/assets/images/mona/floor-surface.jpg' | relative_url }}){: style="max-height: 200px;" }

  Make sure your robot’s wheels have good traction and your vision system can handle light reflections off smooth flooring.

- **Obstacles**  
  There are **no physical obstacles** in the maze. The challenge lies in the layout and navigation alone.  
  Only **black tape** is used to mark the path on the floor surface — no ramps, curbs, or blockages are involved.

---

## FAQs / Troubleshooting

- Updated throughout the event

---

## Optional Hard Mode

- More info provided later in the event

---

## Resources & References

- **Tutorials & Sample Code**  
  You can find a working example of the **video stream client** used for this task in the following GitHub repository:  
  👉 [aj-floater/camera-streaming-client](https://github.com/aj-floater/camera-streaming-client)

  This script provides a reliable starting point for Task 2 and allows your system to interface with the video stream hosted on the university network.  
  It should serve as a foundation for building your **computer vision solution** — including stream access, frame capture, and marker detection.

- **Forum / Discord**  
  There is **no public discussion forum**, but you are encouraged to ask questions throughout the event.

  - For **any help during the event**, speak to one of the **supervisors in green t-shirts**.
  - If you are having trouble specifically with **camera streaming**, please **speak to Archie** directly.

- **Additional Documentation**  
  Further documentation is available from:
  - [ICE9-Robotics GitHub](https://github.com/ICE9-Robotics) — For Mona Bot hardware and communication protocols  
  - GitHub README files and comments within the provided code  
  - Instructions distributed in the team packet on the day of the hackathon