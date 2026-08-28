---
title: "World Model-Guided VLA Policy"
date: 2026-04-30
author: "Samith Va"
categories: [embodied-ai, world-models]
tags: [VLA, world-model, LIBERO, policy-learning]
summary: "A VLA policy that uses world-model predictions as foresight when generating action chunks for LIBERO tasks."
showToc: true
draft: false
---

## Overview

This project uses a world model to predict future states and provide foresight for a vision-language-action policy. Predicted states condition VLA action-chunk generation, and the resulting policy is evaluated on LIBERO tasks.

{{< media-placeholder type="figure" label="World model-guided policy architecture" caption="Add the architecture diagram connecting observation, future-state prediction, and VLA action generation." >}}

## Key Contributions

- Used a world model to predict future task states.
- Conditioned VLA action-chunk generation on predicted states.
- Evaluated the approach on LIBERO manipulation tasks.

## Evaluation

{{< media-placeholder type="figure" label="LIBERO evaluation results" caption="Add success-rate plots, qualitative rollouts, or comparisons with the baseline policy." >}}

## Demo

{{< media-placeholder type="video" label="Policy rollout video" caption="Add side-by-side LIBERO rollouts or a narrated project demo here." >}}
