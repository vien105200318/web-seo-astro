---
title: "Character Animation - Making Spirits Move"
description: "From static meshes to terrifying movement using Mixamo and custom tweaking"
pubDate: 2024-05-01
tags: ["animation", "art", "technical"]
image: "/images/blog/023-cover.jpg"
---

# Character Animation - Making Spirits Move

## The "Potato Sack" Problem

My friends laughed at the ghost because she T-posed or slid around.
Need proper animation.

## Mixamo to the Rescue

I can't animate. Adobe Mixamo is a lifesaver.
- Downloaded "Zombie Walk", "Scary Idle", "Scream".
- Retargeted to my Miss Nam model.

## The Uncanny Valley

Standard zombie animations look... generic.
I need "Vietnamese Ghost" movement.
- Floating?
- Twitching?
- Broken limbs?

## Customizing via Code

Used **Procedural Animation** on top of Mixamo.
- Added a script to twitch the head randomly.
- `transform.position.y += sin(time)` for floating effect.
- IK (Inverse Kinematics) to make feet stick to ground (or not).

## The Result

She now floats slightly off the ground. Her head snaps unnaturally.
She doesn't look like a generic zombie anymore.
She looks wrong. In a good way.
