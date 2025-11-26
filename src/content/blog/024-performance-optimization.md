---
title: "Performance Optimization: Fighting The Lag"
description: "Laptop cũ không chịu nổi → học optimize from scratch"
pubDate: 2024-05-10
tags: ["optimization", "performance", "technical"]
image: "/images/blog/024-cover.jpg"
---

# Performance Optimization

## The Crisis

Build chạy 25 FPS trên laptop tôi. Unplayable.

## Optimizations

### Graphics
- LOD system cho 3D models
- Occlusion culling
- Baked lighting thay vì real-time where possible
- Reduce shadow distance

### Code
- Object pooling cho particles
- Coroutines thay vì Update() nếu có thể  
- Garbage collection optimization

### Result

60 FPS stable! Game chạy smooth.

## Lesson

Optimization không phải "about sau". It's core development.
