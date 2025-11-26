---
title: "Performance Optimization - 60 FPS or Die"
description: "Optimizing for low-end hardware because not everyone has an RTX 4090"
pubDate: 2024-05-08
tags: ["optimization", "performance", "technical"]
image: "/images/blog/024-cover.jpg"
---

# Performance Optimization - 60 FPS or Die

## The Lag

My laptop (GTX 1050) was struggling. 25 FPS in the yard.
Unacceptable. Horror needs smooth frames.

## The Culprits

Profiler showed:
1. **Realtime Lights**: Too many point lights casting shadows.
2. **Overdraw**: Too many transparent particles (fog).
3. **Batches**: 2000 draw calls.

## The Fixes

### 1. Light Baking
Baked everything static. Only flashlight is realtime.
FPS: 25 → 40.

### 2. Occlusion Culling
Configured Occlusion Culling so Unity doesn't render what's behind walls.
FPS: 40 → 50.

### 3. GPU Instancing
Enabled GPU Instancing for trees and grass materials.
FPS: 50 → 65.

### 4. LOD (Level of Detail)
Created LODs for high-poly furniture.
FPS: Stable 60+.

## Lesson

**Optimize early.** Don't wait until the end.
Now the game runs on my potato laptop. It will run on players' machines.
