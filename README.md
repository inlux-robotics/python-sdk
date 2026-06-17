# Fairino Cobot Python SDK Integration Guide (Linux/Ubuntu)

This repository provides the core Python SDK architecture, and motion control scripts for Fairino collaborative robots within a Linux environment.

## Repository Structure

```bash
📦 fairino-python-sdk-main
┗ 📂 linux                     # Primary Linux/WSL deployment context
  ┣ 📂 fairino                 # Core SDK initialization layers
  ┣ 📂 libfairino              # Background binary architecture mapping
  ┣ 📂 example                 # Pre-engineered manufacturer reference suite
  ┃ 
  ┣ 📜 test_movement.py        # Verified trajectory integration validation script
  ┗ 📜 test_robot.py           # Primary communication and interface diagnostic script
```

---

## Technical Prerequisites

Before deploying the motion control scripts, establish the baseline environment execution requirements using Python 3 and standard network connectivity parameters:

```bash
sudo apt update
sudo apt install python3 python3-pip -y
```

Execution Protocol and API Integration

Launching the Application
Execute the target script directly from the project root directory using the local python3 interpreter:

```bash
cd linux/
python3 test_movement.py
```

Output Logs Verification
Upon execution, successful verification sequences will dump the initialization stack mapping without triggering memory or trace errors:

The following deployment scenarios validate the trajectory profiles included in this SDK distribution over physical testing platforms:

1. Continuous Path Blending
Demonstrates multi-axis path smoothing using linear (MoveL) and articular (MoveJ) primitives configured under strict velocity overrides and blend matrices (blendMode/blendR).

[![Watch the video](https://img.youtube.com/vi/CozXwgoSC2s/0.jpg)](https://youtu.be/CozXwgoSC2s)

2. Advanced Spiral Path Toolpath
Showcases tool coordinate system offsets (offset_flag=2) paired with dynamic spiral interpolation (NewSpiral) used for orbital tracking and surface processing routines.

[![Watch the video](https://img.youtube.com/vi/cKOAUhq4eBk/0.jpg)](https://youtu.be/cKOAUhq4eBk)
