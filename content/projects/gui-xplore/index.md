---
title: "GUI-Xplore: Empowering Generalizable GUI Agents with One Exploration"
date: 2025-03-22
author: "Samith Va"
categories: [multimodal-ai, gui-agents]
tags: [GUI-Xplore, GUI-agents, exploration, vision-language-models, graph-reasoning]
summary: "We introduce GUI-Xplore, a dataset and framework for learning about unfamiliar apps through exploration videos."
showToc: true
draft: false
cover:
  image: exploration-paradigm.png
  alt: "GUI-Xplore uses an app exploration video to guide reasoning in unfamiliar applications."
  relative: true
  hiddenInSingle: true
---

## Overview

We introduce **GUI-Xplore**, a dataset for improving GUI agents' ability to generalize across apps and tasks. By learning from a recorded exploration of an unfamiliar app, agents gain context about its screens, functions, and interaction patterns before answering task-specific questions.

This work was part of my undergraduate research in early 2025, supervised by Prof. Chongyang Zhang.

**Authors:** Yuchen Sun, Shanhui Zhao, Tao Yu, Hao Wen, **Samith Va**, Mengwei Xu, Yuanchun Li, Chongyang Zhang.

[Read the paper](https://arxiv.org/abs/2503.17709)

[![Comparison of conventional GUI agents and GUI-Xplore: exploration videos provide app-specific context for reasoning across multiple tasks.](exploration-paradigm.png)](exploration-paradigm.png)

*Exploration provides app-specific knowledge to guide reasoning in unfamiliar interfaces (Figure 1).*

## Dataset and tasks

We collect exploration data from **312 apps** and build **32,569 question-answer pairs** across five tasks: application overview, page analysis, application usage, action recall, and action sequence verification. Together, these tasks evaluate understanding of both app functionality and interaction sequences.

## Xplore-Agent

We propose **Xplore-Agent**, a two-stage framework that extracts keyframes and actions from exploration videos, then organizes screens into a **GUI transition graph**. The graph captures how pages connect and guides language-model reasoning across the five tasks.

[![Xplore-Agent pipeline: exploration video, action-aware keyframe extraction, view hierarchy and action generation, GUI clustering, transition graph, and language-model reasoning.](xplore-agent-pipeline.png)](xplore-agent-pipeline.png)

*Xplore-Agent converts exploration videos into a GUI transition graph for reasoning (Figure 3).*

## Results

On our cross-app automation test set of **500 operations across 20 apps**, Xplore-Agent achieves a **30.39% step success rate**, compared with 15.80% for CogAgent. Across the five question-answering tasks, it reaches **64.24% average accuracy**, compared with 59.39% for the best evaluated GPT configuration. Action recall and sequence reasoning remain challenging, highlighting opportunities for better interaction understanding.

*Figures and results are from the linked GUI-Xplore paper, arXiv:2503.17709v1 (2025).*
