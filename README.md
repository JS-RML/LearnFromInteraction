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

## 3. Training

If you want to train your own model, please run the following code:
```
python main.py --play-only==False
```

## 4. Testing
### 4.1 Test in Simulation
We provide a testing script to evaluate our trained model in simulation. The following code runs the test on three trained objects, and report the average grasp success rates.
```
python main.py --play-only==True
```

### 4.2 Test on Real Robot (UR10)
Here we provide the steps to test our method on a real robot.

**Robot control**

Robot is controlled via [this python software](https://github.com/SintefManufacturing/python-urx).

**Camera setup**

To deploy RealSense L515 camera,
1. Download and install the [librealsense SDK 2.0](https://github.com/IntelRealSense/librealsense)
2. Our camera setting can be found in ```real/640X480_L_short_default.json```

**Start testing**

Then run the following code to start testing:
```
cd real
python test_in_real.py
```

## Maintenance 
For any technical issues, please contact: Chao Zhao (czhaobb@connect.ust.hk).
