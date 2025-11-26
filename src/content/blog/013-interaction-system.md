---
title: "Interaction System - Touching the World"
description: "Building a flexible interaction system for doors, items, and clues"
pubDate: 2024-03-10
tags: ["development", "system", "interaction"]
image: "/images/blog/013-cover.jpg"
---

# Interaction System

## Design

I want a system where I can look at an object, see a prompt, and press 'E' to interact.
- Doors: Open/Close.
- Items: Pick up/Examine.
- Lights: Turn on/off.
- Drawers: Slide out.

## Interface Approach

Created `IInteractable` interface:

```csharp
public interface IInteractable
{
    string GetDescription();
    void Interact();
}
```

Any object implementing this can be interacted with.

## Raycasting

In `PlayerInteract.cs`:
- Cast a ray from camera center forward.
- Range: 2.5 meters (short reach).
- If hit object has `IInteractable`, show UI prompt.
- If Input 'E', call `Interact()`.

## The Door Problem

Doors are always harder than they look.
- Rotating door? Physics door? Animation door?
- Went with **Animation** for reliability.
- Created `Door` script implementing `IInteractable`.
- Triggers Animator bool "IsOpen".

## Testing

Placed a cube. Script: `Debug.Log("Touched cube")`.
Walk up. "Press E to Interact". Press E. Log appears.

**It feels like a game now.**
