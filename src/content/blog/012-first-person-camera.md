---
title: "First Person Camera - Seeing Through Character's Eyes"
description: "Implementing a physics-based first person controller"
pubDate: 2024-03-05
tags: ["development", "camera", "gameplay"]
image: "/images/blog/012-cover.jpg"
---

# First Person Camera

## Choosing a Controller

Should I write from scratch or use assets?
- **Unity Starter Assets**: Good but bloated.
- **RigidBody Controller**: Good for physics interaction.
- **CharacterController**: Classic, easier to control.

Decided to write a custom **CharacterController** based script to learn.

## Implementation

### Mouse Look
Standard implementation:
- Get `Input.GetAxis("Mouse X")` and `Y`.
- Clamp vertical rotation (-90 to 90 degrees) to avoid breaking neck.
- Lock cursor: `Cursor.lockState = CursorLockMode.Locked`.

### Movement
- `Input.GetAxis("Horizontal")` and `Vertical`.
- `Vector3 move = transform.right * x + transform.forward * z`.
- `controller.Move(move * speed * Time.deltaTime)`.

## Head Bob

To make it realistic (and scary), added head bobbing.
- Sine wave based on movement speed.
- Subtle, don't want to make players sick.

## The "Feel"

Tweaked values for hours:
- Walk speed: 3.0 (slow, deliberate).
- Run speed: 5.0 (not too fast, you are not Doomguy).
- Crouch speed: 1.5 (stealth).

## Result

I can walk around a plane with some cubes.
The slow movement speed makes even a blank scene feel tense.

**Next: Interaction System.**
