# LimeLib

![License](https://img.shields.io/github/license/Official-3796B/LimeLib)
![Repo Size](https://img.shields.io/github/repo-size/Official-3796B/LimeLib)
![Last Commit](https://img.shields.io/github/last-commit/Official-3796B/LimeLib)
![Issues](https://img.shields.io/github/issues/Official-3796B/LimeLib)
![VEX](https://img.shields.io/badge/Platform-VEX%20V5-red)
![PROS](https://img.shields.io/badge/Built%20With-PROS-blue)
![LemLib](https://img.shields.io/badge/Extension-LemLib-green)

LimeLib is an extension layer for LemLib designed for use with PROS-based VEX V5 robots.

It provides additional tools and structure for robotics codebases, including sensor-assisted localization, organized robot configuration, and utilities for building autonomous routines. LimeLib is designed to integrate with LemLib without modifying its source code.

---

## Features

### Custom Localization System

LimeLib introduces a localization module that supplements LemLib odometry.

Features include:

- Distance-sensor–based field positioning  
- Sensor fusion between odometry and distance measurements  
- Configurable field bounds  
- Weighted blending of sensor measurements  

This allows robots to correct their position relative to field walls for improved autonomous accuracy.

---

### Distance Sensor Integration

The localization system supports multiple distance sensors with configurable placement.

Capabilities include:

- Sensor mounting position configuration  
- Directional field measurements  
- Conversion between measurement units  
- Pose correction blending  

This is useful for:

- Autonomous position correction  
- Wall alignment  
- Field-aware positioning  

---

### Robot Configuration System

LimeLib provides a structured approach to configuring the robot hardware and drivetrain.

Example layout:

src/
├─ robot_config.cpp
├─ chassis_config.cpp
└─ main.cpp


This separates:

- drivetrain configuration  
- robot hardware definitions  
- control logic  

making projects easier to maintain and reuse.

---

### Autonomous Structure

LimeLib includes a simple structure for organizing autonomous routines: src/autos.cpp


Typical program flow:

main.cpp
↓
autos.cpp
↓
chassis + localization systems


---

## Project Structure

LimeLib
│
├─ include/
│ └─ localization.h
│
├─ src/
│ ├─ main.cpp
│ ├─ robot_config.cpp
│ ├─ chassis_config.cpp
│ ├─ localization.cpp
│ └─ autos.cpp
│
├─ firmware/
└─ project.pros


---

## Design Goals

- Extend LemLib without modifying its source  
- Improve autonomous consistency  
- Provide reusable robot architecture  
- Enable field-aware localization  

---

## Requirements

- PROS  
- LemLib  
- VEX V5 hardware platform  

---

## Future Goals

Planned expansions for LimeLib include:

- Advanced sensor fusion  
- Autonomous path utilities  
- Motion helper functions  
- Debugging and telemetry tools  
- Additional chassis helpers  

---

## License

This project follows the same open-source philosophy as LemLib and is intended for use by robotics teams developing competitive software.

