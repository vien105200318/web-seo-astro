---
title: "UI/UX Design - Horror Minimalism"
description: "Designing a user interface that doesn't break immersion"
pubDate: 2024-03-15
tags: ["design", "ui", "ux"]
image: "/images/blog/014-cover.jpg"
---

# UI/UX Design - Horror Minimalism

## Philosophy

**Diegetic UI** is the goal.
- No health bars floating.
- No minimap.
- No objective markers.

## Implementation

### Reticle
- A tiny dot in center.
- Changes to a small hand icon when looking at interactables.
- Opacity: 50%.

### Inventory
- Not a grid.
- A 3D view of the bag? Too complex.
- Compromise: Simple slot bar at bottom, fades out when not used.

### Documents
- When reading a letter, show the actual texture of the paper on screen.
- Font: Handwriting style (Vietnamese font support is a pain).

### Sanity
- Instead of a bar, use **Vignette** and **Chromatic Aberration**.
- Screen gets darker and distorted as sanity drops.
- Heartbeat sound increases.

## Font Choice

Selected **"Playfair Display"** for titles (elegant, old) and **"Inter"** for readability.
Found a great handwritten font for notes that supports Vietnamese accents!

## Result

Clean screen. Nothing between player and the horror.
Just darkness and a tiny white dot.
