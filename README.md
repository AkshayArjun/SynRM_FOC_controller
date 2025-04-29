# SynRM & BLDC motor control methods

This project provides an overview and implementation details for controlling **Synchronous Reluctance Motors (SynRM)** and **Brushless DC Motors (BLDC)**. It discusses control strategies, mathematical modeling, and algorithm development, with a focus on precision, efficiency, and real-world deployment.

---

## Overview

| Feature                 | SynRM                                               | BLDC                                              |
|-------------------------|------------------------------------------------------|---------------------------------------------------|
| Motor Type              | Reluctance-based, no magnets                        | Permanent magnet-based, electronically commutated |
| Rotor Structure         | Laminated iron core, no windings or magnets         | Rotor with embedded or surface-mounted magnets    |
| Torque Production       | Reluctance torque                                   | Electromagnetic torque via back-EMF interaction    |
| Complexity of Control   | High (non-linear, requires advanced algorithms)     | Moderate (depending on commutation technique)     |
| Applications            | Industrial drives, pumps, compressors              | Robotics, automotive, HVAC, appliances            |

---




## Control Methods

### SynRM Control Techniques
- **Field Oriented Control (FOC)**
  - Decouples torque and flux control.
  - Improves dynamic performance and efficiency.
  - Requires rotor position estimation or sensing.
 
### BLDC Control Techniques
- **Six-Step Commutation (Trapezoidal Control)**
  - Simplified commutation based on three Hall sensors.
  - Common in industrial and automotive applications.
  
## Implementation Details

- Development based on microcontrollers supporting high-frequency PWM and ADC sampling.
- Use of Clarke and Park transformations for vector control strategies.
- Closed-loop PI/PI^2 controllers for current, speed, and position regulation.
- Position estimation using observers like Sliding Mode Observer (SMO) or Extended Kalman Filters (EKF) in sensorless designs.



![Screenshot 2025-04-23 211910](https://github.com/user-attachments/assets/459f4448-bdaa-4a18-9267-e006b5228a1c)

![image](https://github.com/user-attachments/assets/0fe11de0-a393-4656-af2d-5c831fecc8ee)
