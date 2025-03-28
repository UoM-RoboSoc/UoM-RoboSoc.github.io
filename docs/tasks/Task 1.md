---
title: Toxic Waste Disposal
parent: Tasks
layout: default
nav_order: 1
---

# Toxic Waste Disposal

A critical mission awaits: your robot must transport a microcontroller-equipped “toxic waste” barrel through an obstacle course before it goes critical. The course features a **dark box**, a **20° ramp**, and a **grass square**, each adding its own challenge. Your goal? Collect and securely place the barrel without jostling it beyond a safe threshold—and get your robot back to the start before time runs out.

---

## Rules & Scoring

- **Time Limit**  
  You have **5 minutes** to complete your run. The timer starts as soon as your robot **crosses into** the marked **Start Square** on the floor and stops when it **fully returns** to that same square.

- **Allowed Interventions**  
  **No pausing** is allowed during the run. We have limited time and pausing would disrupt the flow of the event. In rare “extreme” situations (e.g., total battery failure), staff may allow a brief fix at their discretion, but your robot should be robust enough to avoid these issues.

- **Penalties & Points**  
  Details on **scoring** (including jostling thresholds for the toxic barrel) and any **penalties** will be published separately in the **Judging** section during the hackathon. Keep an eye out for updates!

---

## Arena & Obstacles

| ![Dark Box]({{ '/assets/images/arena/dark-box.jpg' | relative_url }}) | ![20° Ramp]({{ '/assets/images/arena/ramp.png' | relative_url }}) | ![Grass Square]({{ '/assets/images/arena/grass-square.png' | relative_url }}) |
|:---:|:---:|:---:|
| **Dark Box** <br> Size: (e.g. 1m³) <br> Lighting: Very dim <br> Access: Single door on one side | **20° Ramp** <br> Height: ~1m (20° incline) <br> Surface: Wood or acrylic <br> Approach: 30cm run-up | **Grass Square** <br> Surface: Artificial turf <br> Friction: Medium-High <br> Dimensions: 50cm x 50cm |

---

## Kit Contents

| Item     | Description           |
|----------|-----------------------|
| ![Arduino Uno]({{ '/assets/images/kit/arduino-uno.png' | relative_url }}){:style="max-height:100px;"}<br>**Arduino Uno**| A classic microcontroller board for prototyping. Usually 5V logic; great for sensor hookups and basic control logic.|
| ![ESP32 Camera Module]({{ '/assets/images/kit/esp32-cam.png' | relative_url }}){:style="max-height:100px;"}<br>**ESP32 Camera Module** | Provides on-board Wi-Fi, Bluetooth, and camera functionality. Great for streaming video or applying simple computer vision tasks.|
| ![Motor]({{ '/assets/images/kit/motor.png' | relative_url }}){:style="max-height:100px;"}<br>**Motors** | Basic DC motors for driving wheels or other mechanisms. You’ll likely receive 2–4 of these, depending on your rover configuration. |
| ![Wheels]({{ '/assets/images/kit/wheel.png' | relative_url }}){:style="max-height:100px;"}<br>**Wheels** | Accompanying wheels to attach to the motors. |
| ![Motor Driver]({{ '/assets/images/kit/motor-driver.png' | relative_url }}){:style="max-height:100px;"}<br>**Motor Driver Breakout Board** | The l293d module. Handles current flow to your motors. Attach it to the Arduino/ESP32 for motor control signals. |
| ![SG90 Servo]({{ '/assets/images/kit/sg90-servo.png' | relative_url }}){:style="max-height:100px;"}<br>**Servos (SG90)** | Small, lightweight servos. Often used for steering or simple grippers. Supplied in packs of 2–4. |
| ![Bluetooth HC-05]({{ '/assets/images/kit/hc05.png' | relative_url }}){:style="max-height:100px;"}<br>**HC-05 Bluetooth Module** | Allows simple serial communication over Bluetooth. Useful for sending instructions wirelessly. |
| **Battery Case**                                | Holds AA batteries for powering your circuit.                            |
| **AA Batteries**                                | Basic 1.5V cells (quantity depends on your kit).                        |
| **USB-B Cable**                                 | Used for programming and providing power to the Arduino Uno.            |
| **Micro USB Cable**                             | For programming the ESP32 Camera Module.                                |
| **Jumper Wire Pack** <br>(MM, MF, FF)           | Essential for quick prototyping and connecting components on breadboards.|


## Additional Items

Need extra sensors, parts, or specialized tools? Request them through the standard inventory parts procedure.  
👉 [View the full inventory]({{ '/inventory' | relative_url }})

## Modifications

We **encourage creativity**! Feel free to **3D-print** custom parts (no special approvals required, beyond standard [3D Printing Guidelines]({{ '/3d-printing' | relative_url }})). You can even head to Tesco and build your chassis out of a **meal deal sandwich box** — no problem.

- **No Weight Limits:** However, remember the robot needs to fit through the **Dark Box** entrance. We’ll publish recommended size limits once we finalize the Dark Box dimensions.  
- **Go Wild:** As long as you stay safe, your design approach is up to you!

---

## Safety & Handling

- **Barrel Handling**  
  There are **no strict pick-up or drop-off guidelines**—your primary goal is to **minimize side-to-side movement** and **avoid dropping or throwing** the barrel. Any excessive jostling or unsafe handling may lead to **point deductions** (details to be released in the scoring guidelines).

- **Recovery Procedures**  
  If the barrel **is dropped** but stays within the sensor’s acceptable threshold, **no penalty** is applied. However, repeated or severe drops may register on the microcontroller, potentially incurring future deductions.

- **Monitoring Tools**  
  You have **full access** to:
  - **Bluetooth** communication with your robot and the barrel’s microcontroller.  
  - **Wi-Fi** features on the ESP32 Camera Module (e.g., for video streaming).  

Feel free to integrate real-time data into your control system—just keep the barrel’s movement gentle!  

---

## Practice & Testing

- **Arena Access Times**  
  Once the arena is fully assembled, it will be **open for practice**. Feel free to come by anytime to test your robot’s movement and barrel-handling strategies.

- **Booking / Sign-Up**  
  For **official judging**, teams only need to **provide their team name**; the order of attempts will be **randomly assigned** once everyone has signed up. Otherwise, there’s **no formal booking** system for practice—you can just show up.

- **Limitations**  
  Currently, **no specific restrictions** (e.g., max attempts or time slots) have been set for practice sessions. We’ll notify participants via announcements if any become necessary.

---

## Submission & Demo

- **Code Submission**  
  There’s **no official requirement** to submit your code. However, if you’ve built something especially cool and want to share it, feel free to show it off or upload it somewhere (e.g., GitHub) and let others know.

- **Judging Format**  
  We’ll run a **final demonstration** (“final run”) for each team. If your robot fails at that time, unfortunately there won’t be a second attempt—too many teams, too little time! So make sure everything is reliable before your slot.

- **Results & Feedback**  
  **Winners** and **feedback** will be announced during the **closing ceremony** (see the [Schedule]({{ '/schedule' | relative_url }})) along with prize presentations. Keep an eye on announcements for any last-minute details.

---

## Tips & Common Mistakes

- *(Quick bullet points or FAQs about typical challenges, e.g., ramp friction, battery life, sensor calibration, etc.)*
- This will be updated as the event proceeds

---

## Resources & References

- *(Links to tutorials, official docs, or example code if provided.)*
- This will be updated as the event proceeds