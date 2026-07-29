# multimodal-dataset-generation-of-wind-farm-turbines
This repository presents a framework for generating synchronized multimodal datasets in a simulated wind farm environment. The framework supports UAV-based inspection research by acquiring RGB images, thermal images, and LiDAR point clouds from a virtual aerial platform.

![image alt](https://github.com/KarimaHaloua/multimodal-dataset-generation-of-wind-farm-turbines/blob/main/data_acquisition.png?raw=true)

## Overview

This repository presents a framework for generating synchronized multimodal datasets from a simulated UAV operating in a virtual wind farm environment.

The framework enables the acquisition of RGB images, thermal images, and LiDAR point clouds under controlled and repeatable simulation conditions. The generated data is intended to support research in autonomous aerial inspection, computer vision, robotics, and artificial intelligence.

The simulation environment used for data acquisition is documented in the companion repository:

➡️ **Wind Farm Simulation Environment**

---

# Motivation

Publicly available datasets for wind turbine inspection remain limited, particularly for multimodal sensing.

Simulation provides a flexible alternative that enables:

- Safe experimentation
- Controlled environmental conditions
- Repeatable data acquisition
- Scalable dataset generation
- Cost-effective research and development

Synthetic datasets can accelerate the development and evaluation of perception algorithms before deployment in real-world environments.

---

# Objectives

The framework has been developed to:

- Generate synchronized multimodal datasets.
- Acquire RGB images.
- Acquire thermal images.
- Acquire LiDAR point clouds.
- Organize data into reproducible datasets.
- Support robotics and AI research for infrastructure inspection.

---
# Framework Architecture

The dataset generation framework is built upon a modern robotics software stack that combines high-fidelity simulation, autonomous flight control, and robotic middleware.

| Component | Description |
|------------|-------------|
| Blender | Wind farm modeling |
| Gazebo Sim | Physics-based simulation |
| PX4 SITL | UAV flight controller |
| ROS 2 Jazzy | Middleware and communication |
| QGroundControl | UAV mission control |
| RViz2 | Data visualization |
| Docker | Containerized execution |

The interaction between these components enables the execution of autonomous UAV missions and the acquisition of synchronized multimodal data within a realistic simulation environment.

The simulation runs inside a Docker container on Ubuntu 24.04.

# Sensor Configuration
We are used the default x500 vision drone (PX4 model) and add 3d lidar sensor and thermal Camera.

The framework supports three complementary sensing modalities.

| Sensor | Output |
|---------|--------|
| RGB Camera | Color Images |
| Thermal Camera | Thermal Images |
| LiDAR | 3D Point Clouds |

These sensing modalities provide complementary information for perception and inspection tasks.

---
## TF Generation

To ensure spatial consistency, odometry data are converted into TF frames using a custom ROS 2 Python node.

The resulting TF tree is recorded together with the sensor data.

Recorded information includes:

- TF
- Static TF
- UAV Odometry

# Synchronization

The generated datasets are organized using synchronized sensor observations.

The framework ensures temporal consistency between the different sensing modalities, facilitating future research on:

- Sensor Fusion
- Multi-modal Perception
- 3D Scene Understanding
- Autonomous Navigation

---

## Dataset Recording

All sensor streams are synchronized and recorded into a single ROS 2 bag.

The recorded data include:

- RGB Images
- Thermal Images
- LiDAR Scans
- TF
- Static TF

---


# Sample Outputs
The recorded data can be visualized in RViz2.

![image alt](https://github.com/KarimaHaloua/multimodal-dataset-generation-of-wind-farm-turbines/blob/main/Multimodal_data.png?raw=true)

![image alt](https://github.com/KarimaHaloua/multimodal-dataset-generation-of-wind-farm-turbines/blob/main/Lidar%20data.png?raw=true)

![image alt](https://github.com/KarimaHaloua/multimodal-dataset-generation-of-wind-farm-turbines/blob/main/RGB%20data.png?raw=true)

![image alt](https://github.com/KarimaHaloua/multimodal-dataset-generation-of-wind-farm-turbines/blob/main/Thermal%20data%20.png?raw=true)

---

# Potential Applications

The generated datasets can support research in:

- Infrastructure Inspection
- Autonomous UAV Navigation
- Computer Vision
- Object Detection
- Semantic Segmentation
- Defect Detection
- Sensor Fusion
- Multi-modal Learning
- SLAM
- 3D Scene Understanding

---


# Research Context

This repository is part of an ongoing PhD research project investigating simulation-based methodologies for multimodal dataset generation using autonomous UAVs for wind turbine inspection.

The generated datasets will support future research in autonomous inspection, perception, and artificial intelligence.

---

# Associated Simulation Platform

The simulation environment used to generate these datasets is documented in the companion repository:

➡️ **Wind Farm Simulation Environment**

---


