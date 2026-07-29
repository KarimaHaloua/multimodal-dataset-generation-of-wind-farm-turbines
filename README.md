# multimodal-dataset-generation-of-wind-farm-turbines
This repository presents a framework for generating synchronized multimodal datasets in a simulated wind farm environment. The framework supports UAV-based inspection research by acquiring RGB images, thermal images, and LiDAR point clouds from a virtual aerial platform.
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

| Component | Role |
|-----------|------|
| **Gazebo Sim** | Physics-based simulation environment |
| **PX4 SITL** | UAV flight controller simulation |
| **ROS 2 Jazzy** | Communication middleware and data management |
| **RViz2** | Visualization and monitoring |
| **Python / C++** | Framework development |

The interaction between these components enables the execution of autonomous UAV missions and the acquisition of synchronized multimodal data within a realistic simulation environment.
# Sensor Configuration

The framework supports three complementary sensing modalities.

| Sensor | Output |
|---------|--------|
| RGB Camera | Color Images |
| Thermal Camera | Thermal Images |
| LiDAR | 3D Point Clouds |

These sensing modalities provide complementary information for perception and inspection tasks.

---

# Synchronization

The generated datasets are organized using synchronized sensor observations.

The framework ensures temporal consistency between the different sensing modalities, facilitating future research on:

- Sensor Fusion
- Multi-modal Perception
- 3D Scene Understanding
- Autonomous Navigation

---

# 📂 Dataset Organization

The generated dataset follows a structured organization.

```text
Dataset/

├── RGB/
│     ├── image_000001.png
│     ├── image_000002.png
│     └── ...
│
├── Thermal/
│     ├── thermal_000001.png
│     ├── thermal_000002.png
│     └── ...
│
├── LiDAR/
│     ├── cloud_000001.pcd
│     ├── cloud_000002.pcd
│     └── ...
│
└── Metadata/
      ├── timestamps.csv
      └── sensor_information.json
```

---

# 🖼 Sample Outputs

## RGB Images

<p align="center">
<img src="images/rgb_sample.png" width="750">
</p>

---

## Thermal Images

<p align="center">
<img src="images/thermal_sample.png" width="750">
</p>

---

## LiDAR Point Clouds

<p align="center">
<img src="images/lidar_sample.png" width="750">
</p>

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


