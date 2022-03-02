# Learn from Interaction: Learning to Pick via Reinforcement Learning in Challenging Clutter

## 1. Overview
In this work, we present an end-to-end reinforcement learning (RL) framework, which aims at singulating and simultaneously picking the objects one by one from a random clutter. We present a novel solution to incorporate object interaction in policy learning and a gripper designed for this technique is capable of changing relative digit lengths. This repository provides the implementation.

## 2. Prerequisites
### 2.1 Hardware requirements
- [**Universal Robot UR10**](https://www.universal-robots.com/products/ur10-robot/)
- [**Robotiq 140mm Adaptive parallel-jaw gripper**](https://robotiq.com/products/2f85-140-adaptive-robot-gripper)
- [**RealSense Camera L515**](https://www.intelrealsense.com/lidar-camera-l515/)
- **Extendable Finger** for realizing the adjustable finger length. The CAD model can be found [here](https://hkustconnect-my.sharepoint.com/:f:/g/personal/ztong_connect_ust_hk/ElzIJrD7_SBMmZwoY-N5tyMB4VmvTVLndxHhNvtrc3OMmw?e=mrNvPl). 

### 2.2 Software requirements
The code is built with Python 3.6. Dependencies are listed in [[requirements.yaml](https://github.com/HKUST-RML/Learning-to-Grasp-by-Digging_v2/blob/main/requirements.yaml "requirements.yaml")] and can be installed via [Anaconda](https://www.anaconda.com/) by running:

    conda env create -n learn_interaction -f requirements.yaml
