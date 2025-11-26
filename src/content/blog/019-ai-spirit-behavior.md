---
title: "AI Spirit Behavior - Not Just Chasing"
description: "Coding AI that stalks rather than attacks"
pubDate: 2024-04-10
tags: ["ai", "coding", "gameplay"]
image: "/images/blog/019-cover.jpg"
---

# AI Spirit Behavior - Not Just Chasing

## The Problem with Chasing

Standard horror AI: See player → Run at player → Kill.
Boring. Predictable.

## The "Stalker" AI

I want the ghost (Miss Nam) to be unsettling.

### States
1. **Idle**: Invisible, wandering waypoints.
2. **Stalk**: Teleport to a location *behind* player or *just out of view*.
3. **Observe**: Watch player from distance. If player looks → Vanish.
4. **Warn**: If player breaks taboo → Audio warning, lights flicker.
5. **Punish**: Only attack if warnings ignored.

## Implementation

Used **NavMesh** for movement.
But added a "Visibility Manager":
- `OnBecameVisible`: If camera sees ghost, trigger vanish timer.
- `Teleport`: Find point on NavMesh behind player camera.

## The "Weeping Angel" Effect

Implemented a mechanic where she only moves when you DON'T look.
- Raycast check every frame.
- If seen: Stop moving (or vanish).
- If not seen: Move closer.

## Result

I was testing the "Stalk" state.
I turned around in game. She was standing there, under the banyan tree, just looking.
I didn't code a jumpscare. She just stood there.
My heart skipped a beat.

**Unpredictability is the key to horror.**
