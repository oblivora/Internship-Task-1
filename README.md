# Drone Technology & UAV Systems Internship - Task 1(Part 3-5)
**By:** Kumar Aman  
**Email:** [aman0arc@gmail.com](mailto:aman0arc@gmail.com)





## PART-3: First Drone Connection Script

### Terminal Execution Screenshot
<p align="center">
  <img width="1465" height="410" alt="Screenshot 2026-03-18 005255" src="https://github.com/user-attachments/assets/b959d61f-63f6-4004-923d-1894c1ca4d46" />

</p>

**Technical Explanation:**
* **SUCCESS! Message:** Confirms a stable MAVLink handshake between the Python script and ArduPilot SITL.
* **GPS Status:** `fix=6, num_sat=10`. A fix of 6 indicates a high-precision 3D lock, essential for autonomous navigation.
* **Battery Monitoring:** `voltage=12.6, level=100`. [cite_start]Monitors real-time voltage to prevent power-related failsafes.
* **Heartbeat:** `~0.89s`.Represents the latency of the MAVLink packet stream; values under 1s indicate a healthy connection.

---

## PART-4: Basic Arm and Takeoff (18m)

### Video Demonstration
<p align="center">
  <video>
    

https://github.com/user-attachments/assets/b4c2ae8a-58c7-44b2-9173-1fdf9efee9de


  </video>
</p>

**GUIDED MODE EXPLANATION:**
* GUIDED mode is the primary autonomous flight mode used when a drone is being controlled by an external computer or script, such as DroneKit-Python. Unlike manual modes, GUIDED mode allows the flight controller to ignore RC stick inputs and instead follow specific target coordinates (Latitude, Longitude, and Altitude) sent via MAVLink.
  
**Why 0.95 altitude check is used:**
*In drone programming, specifically when using ArduPilot and DroneKit, the 0.95 altitude check is a logic threshold used to ensure the script does not get stuck in an infinite loop while waiting for the vehicle to reach a specific height

---
# PART-5: Project - 10m x 10m Square Mission

### Autonomous Pattern Video
<p align="center">
  

https://github.com/user-attachments/assets/aeed7b95-bd3f-467d-a062-f99561bb822a


  
</p>

**Mission Objectives:**
1. **Takeoff:** Reach 18m cruise altitude.
2. **Waypoint 1:** Move 10m North.
3. **Waypoint 2:** Move 10m East.
4. **Waypoint 3:** Move 10m South.
5. **Waypoint 4:** Move 10m West (Return to Takeoff Point).
6. **Land:** Autonomous descent and motor disarming.

---
