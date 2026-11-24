---
title: "Can an Agent's Judgment Improve from Experience?"
description: Testing whether a world-model-trained agent makes better decisions when it keeps falsifiable beliefs about what it has seen.
date: 2026-11-24
period: Nov 2026 – present
role: Solo project
status: In progress
featured: true
stack: [Python, PyTorch, ALFWorld, LLM agents]
tags: [reinforcement learning, self-improvement, agents]
---

## Motivation

A loop where AI improves AI only works if the system can tell which change is worth trying. I think that judgment is the bottleneck. People get good judgment from experience. Current reinforcement learning, though, mostly gives the model one outcome score per attempt, which is a thin signal to learn from.

So the question for this project is simple: **does an agent's judgment actually get better from experience?**

## Approach

- Start from a publicly released model trained with **WM-PPO**, where the agent also learns to predict what will happen after its actions (a world model). Its weights stay frozen.
- Add **EvoBelief**: the agent keeps explicit beliefs about the environment, each one stated so that later evidence can prove it wrong, and updates them as it goes.
- Run it on **ALFWorld**, a text-based household task benchmark, and compare against the same model without the belief module.

## Status

Experiments are running. This is my senior-team project for Aing, the AI club at Gachon University, with a presentation on December 15, 2026. I'll add results and a write-up here.

<!-- TODO: results table, what worked, what didn't -->
