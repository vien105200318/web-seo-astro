---
title: "First-Person Camera và Cảm Giác Mê Hoặc"
description: "Setup camera system và học về importance của camera feel"
pubDate: 2024-02-28
tags: ["development", "camera", "cinemachine"]
image: "/images/blog/012-cover.jpg"
---

# First-Person Camera

## Cinemachine Magic

Thay vì hardcode camera, dùng Cinemachine - Unity's camera system.

Setup Virtual Camera với:
- Aim: Medium sensitivity
- POV: Mouse X/Y axis control
- Body: Follow player head

## Head Bob

Thêm head bob script để walking cảm giác realistic. Sine wave đơn giản:

```csharp
float bobAmount = Mathf.Sin(Time.time * bobSpeed) * bobMagnitude;
cameraTransform.localPosition = new Vector3(0, defaultY + bobAmount, 0);
```

Test... và instant motion sickness! 😅

Giảm magnitude xuống 50%. Better.

## Field of View Tricks

Run = FOV 75
Walk = FOV 65

Tạo sense of speed mà không cần particle effects.

## Lessons

Camera feel = 50% of game feel. Spend time on this!
