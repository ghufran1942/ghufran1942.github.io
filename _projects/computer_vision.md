---
layout: project
title: "Optimized Vision Pipeline on Jetson Orin"
description: "Built and optimized a computer vision object detection pipeline using YOLOv5 and TensorRT on NVIDIA Jetson Orin."
tech_stack: ["YOLOv8", "TensorRT", "Jetson Orin", "ROS"]
thumbnail: "/assets/img/projects/jetson-pipeline.jpg"
link: "/projects/jetson-pipeline"
date: 2024-07-15
category: robotics
---

## Project Overview

Developed a perception system for low-latency object detection suitable for real-time robotics applications.

## Key Features

- TensorRT acceleration on Jetson Orin
- Custom YOLOv5 integration with ROS
- Real-time bounding box rendering and publishing

## Technical Implementation

Optimized the inference graph, reduced detection time to under 40ms. Deployed using ROS node for camera stream integration.

## Results

Enabled sub-50ms object detection. Achieved stable ROS publishing for downstream planning tasks.
