---
title: Tasks
layout: default
---

# Welcome to the Tasks Section

Below you’ll find an overview of the three main challenges available at Hack-A-Bot 2025. Pick one that sparks your interest or that suits your team’s skills, and dive in!

---

## Table of Contents

1. [Toxic Waste Disposal](#toxic-waste-disposal)
2. [Mona Delivery Bot](#mona-delivery-bot)
3. [Raspberry Pi AI Camera](#raspberry-pi-ai-camera)

---

## Toxic Waste Disposal

There’s a nuclear plant that needs decommissioning, and your mission is to safely “defuse” it before it reaches critical status. Your bot will navigate an obstacle course, dealing with different terrains and challenges (from flat surfaces to ramps and extreme terrains), ultimately picking up and placing hazardous materials in a *secure location*. You’ll have limited time for each challenge, so plan your approach carefully.

**Key Points:**
- Robot starts in a designated spot on the floor; when time is up, it must be back on the spot.
- Each challenge adds complexity (ramp, uneven surfaces, camera usage).
- You’ll need to use the rover kit (plus any additional items you can scrounge up responsibly).

**Toxic Waste Barrels**

Each “toxic waste” barrel is a custom made item containing a microcontroller with accelerometers, gyroscopes, and Bluetooth capability. This setup provides real-time monitoring of the barrel’s movement. If the barrel is jostled beyond a specified threshold, you’ll lose points — so transport it with care!

**Arena Setup**

The course includes:
- **A Dark Box:** Your robot must operate with limited visibility.
- **A 20° Ramp:** Test your rover’s climbing and balancing ability.
- **A Grass Square:** Simulates uneven terrain, challenging your bot’s traction.

Your robot will need to handle all three conditions while safely moving the barrel from start to finish. Good luck!

---

## Mona Delivery Bot

Program the “Mona Bot” to follow a line maze and perform simulated payload pickups and dropoffs at designated spots. A live video feed helps you see the maze from above, but once the system is running, it’s up to your computer vision solution to keep the robot on track and pause in the right spots.

**Key Points:**
- A single-line maze with start, pickup, and dropoff positions.
- Must stop for 2 seconds at each point to simulate picking up/dropping off a “pizza.”
- The more successful delivery cycles, the better your score.
- **Hard Mode:** Multiple drop-off points for higher difficulty (and higher points!).

**Equipment & Setup:**
- Mona Bot with a wireless communication module (e.g., Arduino NRF).
- Overhead camera streaming to a web server, also displayed on a nearby screen.
- The QR codes are fiducial markers that your computer vision system will use to locate the pick-up, drop off and start/end positions.

**Rules & Scoring:**
- Strictly follow the maze line.
- 2-second stops at each pickup/dropoff.
- Extra points for precise stops and more completed cycles.

---

## Raspberry Pi AI Camera

The University is busy with many moving parts. Your goal is to create an innovative solution using a **Raspberry Pi AI Camera** (provided) to assist with tasks like tracking sports teams’ positions and energy levels, or ensuring people in the Makerspace wear the correct safety gear. Sky’s the limit — be creative!

**Ideas & Inspiration**

- **Use on-board AI processing** to detect certain patterns or identify whether someone is wearing protective equipment.  
- **Build a real-time monitoring system** to track and log data (e.g., athlete stats, lab safety compliance, etc.).  
- **Combine sensor inputs** for advanced event detection (e.g., accidents, missing gear).

**Challenge Focus**

- **Real-World Impact:** Show how AI can solve actual campus problems.  
- **Robust Recognition:** Demonstrate strong image recognition or object detection.  
- **IoT & Robotics Integration:** Potential synergy with other robotic or IoT systems.

**Extra Credit**

You’ll earn **bonus points** for creative use of the AI camera **in combination** with any of our specialized components from the hackathon inventory. Think beyond just image capture; integrate sensors, mechanical elements, or additional microcontrollers to create a truly innovative solution.

### Use Case Sharing

Instead of distributing a traditional feedback form, we’re building the **sharing** requirement directly into the challenge. Each team must **post their use case** on a designated platform (we’re considering the official [Raspberry Pi Forum](https://www.raspberrypi.org/forums/) but are open to suggestions) to showcase what you’ve built to the broader community.

To encourage active promotion, we’re introducing a **“Community Winners”** category. **One month** after the hackathon ends, we’ll check which projects get the highest visibility (e.g., most views or shares). The top **two teams** will each receive an **additional prize**. 

This approach helps us amplify your creative work, fosters knowledge-sharing, and underscores our priority: getting your projects seen and discussed by a wider audience. So, once you’ve finished building, **spread the word**—and good luck!  

---

*Got questions or need help choosing a task? Check the sidebar for more details, or ask a volunteer in a green supervisor T-shirt. Good luck!* 