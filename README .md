---
##ARIA - Advanced Robotic Intelligence and Actuation
## Overview  
ARIA is a dual-module robotic control system designed for high-performance basketball-playing robots. It features a **top-bottom motherboard architecture** with auxiliary daughterboards, a Raspberry Pi master controller, and an independent safety monitoring PCB. Built for ruggedness and modularity, this system ensures precise actuation and real-time diagnostics.

---

##   Hardware Architecture  
### 1. **Dual Motherboard Core**  
   - **Top Motherboard**  
     - Manages upper peripherals (e.g., arm actuators, vision sensors).  
     - Runs **micro-ROS** for real-time communication.  
   - **Bottom Motherboard**  
     - Controls lower peripherals (e.g., wheel motors, balance systems).  
     - Connects to Raspberry Pi via USB for centralized command.  

####Full Render 
Top view

![image](https://github.com/user-attachments/assets/f76e31a3-b5dd-4ede-9075-b7fcd2ea3189)



Bottom view


PCB



View 1 -              Top(left)                                                               Bottom(right)



### 2. **Auxiliary Daughterboards**  
   - **Top & Bottom Daughterboards**  
     - Mounted on modular panels for easy access and maintenance.  
     - Handle secondary sensors/actuators (e.g., encoders, grippers).  

Top daughter auxiliary pcbs

Bottom daughter auxiliary pcb


### 3. **Central Control Unit**  
   - **Raspberry Pi** acts as the master controller, housed in a dedicated enclosure.  
   - Orchestrates communication between top/bottom modules.  

---

##  Upgrade PCB: Safety & Diagnostics  
![Upgrade PCB Front](link-to-image) | ![Upgrade PCB Back](link-to-image)  
A standalone board for system health monitoring:  
- **Real-time metrics**: Voltage, temperature, and actuator load.  
- **Fail-safe protocols**: Automatic shutdown on critical thresholds.  
- **Expandable**: Supports custom sensors for advanced safety checks.  

Upgrade PCB
 Front

Back

---

##  Key Features  
- **Modular Design**  
  - Plug-and-play daughterboards for rapid repairs/upgrades.  
  - Separate enclosures for top/bottom components.  
- **Rugged Construction**  
  - IP-rated enclosures with vibration-resistant mounts.  
- **ROS Integration**  
  - Seamless compatibility with robotic middleware.  

---

##  Design Philosophy  
1. **Accessibility**  
   - Daughterboards mounted on external panels for tool-free access.  
2. **Scalability**  
   - Extra GPIO/I2C ports for future expansions.  
3. **Fault Tolerance**  
   - Redundant power lanes and isolated sensor circuits.  

---

##  Safety Notes  
- Always check the Upgrade PCB’s heartbeat LED before operation.  
- Avoid exposing enclosures to temperatures >60°C.  

---

*Designed by 
Ashmit R Sambrani : https://github.com/Ash29062
Rishadd

