---
title: "Lighting - Painting with Darkness"
description: "Setting up volumetric lighting and fog for maximum atmosphere"
pubDate: 2024-03-20
tags: ["graphics", "lighting", "atmosphere"]
image: "/images/blog/015-cover.jpg"
---

# Lighting - Painting with Darkness

## The Importance of Darkness

In horror, what you *don't* see is scarier than what you see.
Lighting is not just illumination; it's concealment.

## Unity URP Setup

### Global Volume
- **Fog**: Exponential Squared. Color: Dark Grey. Density: High.
- **Bloom**: Subtle glow for candles.
- **Vignette**: Darken corners to focus vision.
- **Film Grain**: 0.2 intensity for old movie feel.

### Light Sources

1. **Moonlight**: Directional Light. Color: Pale Blue (#8090A0). Intensity: Low (0.2).
2. **Lanterns/Candles**: Point Lights. Color: Warm Orange (#FF8000).
3. **Flashlight**: Spot Light. Cookie texture added for realism (cracks in lens).

## Volumetric Lighting

Added a "Volumetric Light" feature (using a shader).
- God rays coming through window slats.
- Fog glows around street lamps.

## Baking

Baked lighting for static geometry.
- Realtime GI is too heavy.
- Mixed lighting: Baked ambient, realtime shadows for player.

## The "Vibe" Check

Walked through the test scene.
The contrast between the cold blue moonlight outside and the warm, safe (but flickering) orange candlelight inside is perfect.
It feels lonely. It feels Vietnamese countryside at night.
