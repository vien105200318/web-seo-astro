---
title: "Ritual Mechanic - The Core Gameplay"
description: "Implementing the incense lighting and offering mechanic"
pubDate: 2024-04-05
tags: ["gameplay", "mechanic", "culture"]
image: "/images/blog/018-cover.jpg"
---

# Ritual Mechanic - The Core Gameplay

## The Concept

Instead of shooting zombies, you appease spirits.
The core loop: **Identify Spirit → Find Offering → Perform Ritual**.

## Implementation: Lighting Incense

1. **Interaction**: Pick up incense stick.
2. **Lighting**: Hold near candle flame. Particle effect triggers (smoke).
3. **Planting**: Click on incense bowl.

**Challenge**: Hand animation.
- My rigging skills are bad.
- Solution: Floating hands (Rayman style) but hidden by darkness/camera angle.

## The Offering System

Created a `RitualSpot` script.
- Requires specific items (e.g., "Boiled Chicken", "Sticky Rice", "Salt").
- Player must place items in specific slots.
- Check logic: `if (placedItems == requiredItems) Success()`.

## Cultural Nuance

Added a rule: **"Do not plant incense with left hand"**.
- If player uses left hand (control key modifier), ritual fails/angers spirit.
- Subtle cultural detail.

## Testing

It feels meditative yet tense.
Lighting incense in a dark game, watching the smoke rise... it hits a primal chord in Vietnamese culture.
It feels respectful, not just a game mechanic.
