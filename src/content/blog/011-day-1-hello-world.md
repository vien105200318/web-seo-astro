---
title: "Day 1: Hello World (In Unity)"
description: "Setting up the project and writing the first lines of code"
pubDate: 2024-03-01
tags: ["development", "unity", "coding"]
image: "/images/blog/011-cover.jpg"
---

# Day 1: Hello World

## Project Setup

Finally opened Unity Hub.
- **Project Name**: Project_Ma (temporary).
- **Template**: 3D (URP).
- **Version**: 2022.3.10f1 LTS.

Click "Create Project". The waiting bar runs...

## Folder Structure

I learned from experience, need to organize neatly from the start:
```
_Project
  ├── Animations
  ├── Audio
  ├── Materials
  ├── Models
  ├── Prefabs
  ├── Scenes
  ├── Scripts
  │   ├── Core
  │   ├── Player
  │   ├── Systems
  │   └── UI
  └── Textures
```
Underscore `_` to keep my folder at the top.

## First Script

Created `GameManager.cs`.

```csharp
using UnityEngine;

public class GameManager : MonoBehaviour
{
    void Start()
    {
        Debug.Log("Hello World! The nightmare begins.");
    }
}
```

Drag script to an Empty GameObject. Press Play.

Console: `Hello World! The nightmare begins.`

**It works!** (Of course it works, it's one line).

## Git Setup

- `git init`
- Created `.gitignore` for Unity.
- `git add .`
- `git commit -m "Initial commit"`
- Pushed to private GitHub repo.

## Feeling

A small step. But looking at that log line, I feel a strange excitement. The empty void of the scene is now a canvas.

**Tomorrow: First Person Controller.**
