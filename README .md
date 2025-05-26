---
## ARIA - Advanced Robotic Intelligence and Actuation
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

### Full Render 
Top view

![image](https://github.com/user-attachments/assets/f76e31a3-b5dd-4ede-9075-b7fcd2ea3189)



Bottom view

![image](https://github.com/user-attachments/assets/96c68099-ce3e-4a96-8102-f584d76d52f2)



PCB

![image](https://github.com/user-attachments/assets/f1637df8-3a7b-43f0-b00a-e247ec9821e8)



View 1 -              Top(left)                                                               Bottom(right)

![image](https://github.com/user-attachments/assets/7c566b52-dd3a-498e-8748-81b45d8636a5)


### 2. **Auxiliary Daughterboards**  
   - **Top & Bottom Daughterboards**  
     - Mounted on modular panels for easy access and maintenance.  
     - Handle secondary sensors/actuators (e.g., encoders, grippers).  

Top daughter auxiliary pcbs

![image](https://github.com/user-attachments/assets/453e9d1f-de1a-4562-9032-02dd31a6b907)

Bottom daughter auxiliary pcb

![image](https://github.com/user-attachments/assets/8616887c-10ff-4c1b-8f4c-c592323e1c72)


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

![image](https://github.com/user-attachments/assets/b25d8c05-5737-4cd0-a6dc-2cbc278acd9e)


Back

![image](https://github.com/user-attachments/assets/3930da48-36c7-475f-9e82-3ce5ff099bcb)


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

