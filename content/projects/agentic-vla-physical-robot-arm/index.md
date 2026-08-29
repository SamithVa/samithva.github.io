---
title: "Agentic VLA Deployment on a Physical Robot Arm"
date: 2026-08-01
author: "Samith Va"
categories: [embodied-ai, robotics]
tags: [VLA, PiPER, inverse-kinematics, robot-arm]
summary: "An agentic vision-language-action system deployed on a physical PiPER robotic arm for object approach and grasp execution."
showToc: true
draft: false
---

## Overview

This project deploys an agentic vision-language-action (VLA) system on a physical PiPER robotic arm. The system combines inverse kinematics for approaching a target object with VLA-based control for grasp execution.

{{< media-placeholder type="figure" label="System overview" caption="Add a figure showing the agent, perception, planning, and robot-control pipeline." >}}

## Key Contributions

- Deployed an agentic VLA system on a physical PiPER robotic arm.
- Integrated inverse kinematics for object approach.
- Used VLA-based control for grasp execution.

## Results

{{< media-placeholder type="figure" label="Physical robot experiments" caption="Add representative grasping trials, task sequences, or quantitative results." >}}

## Demonstrations

### Cup arrangement

The agentic VLA system identifies and manipulates cups arranged on the work surface.

<figure class="project-video">
  <video controls preload="metadata" playsinline poster="cups-poster.jpg">
    <source src="cups.webm" type="video/webm">
    <source src="cups.mp4" type="video/mp4">
    Your browser does not support embedded video.
  </video>
  <figcaption>Physical robot-arm demonstration with a cup arrangement task.</figcaption>
</figure>

### Opening a drawer

The robot approaches a drawer and executes the opening action with VLA-based control.

<figure class="project-video">
  <video controls preload="metadata" playsinline poster="open-drawer-poster.jpg">
    <source src="open-drawer.webm" type="video/webm">
    <source src="open-drawer.mp4" type="video/mp4">
    Your browser does not support embedded video.
  </video>
  <figcaption>Physical robot-arm demonstration of opening a drawer.</figcaption>
</figure>
