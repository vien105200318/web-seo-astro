---
title: "Day 1: Hello World Trong Unity"
description: "Dòng code đầu tiên và bài học về ego"
pubDate: 2024-02-25
tags: ["development", "unity", "coding"]
image: "/images/blog/011-cover.jpg"
---

# Day 1: Hello World Trong Unity

## Empty Scene

Mở Unity lần đầu như solo dev. Main Camera. Directional Light. Và... nothing else.

## First Script

`PlayerController.cs` - The most important script:

```csharp
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    void Start()
    {
        Debug.Log("Hành trình bắt đầu...");
    }
}
```

Nhấn Play. Console hiện: *"Hành trình bắt đầu..."*

**Tôi đã khóc.**

Nghe dramatic nhưng real. Hai tháng dreaming, giờ finally code chạy.

## Blocking Environment

Không làm gì fancy. Chỉ cubes:
- 1 cube = floor (10x10)
- 4 cubes = walls  
- 1 cube = player (height 1.8)
- ProBuilder để tạo nhà đơn giản

Nhìn như Minecraft. Nhưng đó là **nhà cổ đầu tiên.**

## Basic Movement

Implement WASD movement:

```csharp
void Update()
{
    float h = Input.GetAxis("Horizontal");
    float v = Input.GetAxis("Vertical");
    
    Vector3 direction = new Vector3(h, 0, v);
    transform.Translate(direction * speed * Time.deltaTime);
}
```

Player di chuyển! Hơi giật, không smooth, nhưng it works!

## Bài Học Đầu Tiên

**Perfection kills progress.**

Tôi đã mất 2 giờ trying to make movement "perfect" ngay lần đầu. Cuối cùng realize: Just make it work first, polish later.

## Git First Commit

```
git init
git add .
git commit -m "Day 1: Basic player movement"
```

Cảm giác unreal. Project đã bắt đầu exist trong reality.

**Ngày mai: First-person camera và interaction system.**
