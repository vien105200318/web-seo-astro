---
title: "AI Spirit Behavior: Making Ghosts Feel Alive"
description: "Lập trình hành vi cho linh hồn - cân bằng scary và fair"
pubDate: 2024-04-05
tags: ["AI", "spirit", "behavior"]
image: "/images/blog/019-cover.jpg"
---

# AI Spirit Behavior

## Challenge: Smart Enough To Be Scary, Not Unfair

Spirit cần:
- Unpredictable nhưng consistent
- Scary nhưng escapable
- Reactive to player actions

## Behavior States

### Idle/Patrol
- Wander trong khu vực designated
- Ambient sounds (breathing, whispers)
- Không aggressive

### Investigate
- Hear player noise → đến check
- Search pattern realistic
- Có thể give up

### Chase
- Player spotted / made too much noise
- Fast nhưng marathon không bằng player sprint
- Lose line of sight → switch to investigate

### Ritual State
- Nếu player đang làm ritual correct
- Spirit calms down gradually
- Eventually disappear hoặc become friendly

## Implementation

State machine với transitions based on:
- Distance to player
- Line of sight
- Player noise level (movement + actions)
- Ritual progress

**Tuning AI behavior = 2 weeks nightmare**

Nhưng khi playtest và thấy tester genuinely scared → priceless.
