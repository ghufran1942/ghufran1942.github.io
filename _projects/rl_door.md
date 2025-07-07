---
layout: project
title: "TD3 Reinforcement Learning for Door Opening"
description: "Simulated a robotic arm learning door opening behavior using TD3 algorithm in MuJoCo."
tech_stack: ["Python", "TD3", "MuJoCo", "Gym", "PyTorch", "Apple Silicon"]
thumbnail: "/assets/img/projects/td3-door.jpg"
link: "/projects/td3-door-opening"
date: 2025-06-15
category: robotics
---

## Project Overview

Used TD3 to train a simulated robotic arm to open a door efficiently using reward shaping and exploration tuning.

## Key Features

- Continuous control with TD3
- Simulated in MuJoCo environment
- Performance compared across Apple M2 vs. NVIDIA GPU
- Trained over thousands of episodes

## Technical Implementation

PyTorch implementation of TD3. Real-time policy updates with logging and performance benchmarks. Mac-native training for energy-efficient execution.

## Results

Achieved a 90% success rate. Model converged in ~25% fewer steps on Apple M2 than Jetson/NVIDIA testbed.
