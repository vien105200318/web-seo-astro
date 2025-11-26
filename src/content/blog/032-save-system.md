---
title: "Save System - The Nightmare of Serialization"
description: "Why saving game state is the hardest part of programming"
pubDate: 2024-07-08
tags: ["coding", "system", "technical"]
image: "/images/blog/032-cover.jpg"
---

# Save System - The Nightmare of Serialization

## The Requirement

Player needs to save progress.
- Which night?
- Which items in inventory?
- Which doors are open?
- Where is the ghost?

## JSON vs Binary

Chose **JSON** for easy debugging.
Used `Newtonsoft.Json`.

## The Challenge

You can't just save a GameObject.
You have to create a data class:
```csharp
[System.Serializable]
public class GameData {
    public int currentNight;
    public List<string> inventoryIDs;
    public Vector3 playerPos;
}
```

## The Bug

Loaded game → Inventory empty.
Why? Because I forgot to re-instantiate the items from IDs.
Spent 3 days fixing save/load bugs.
It's boring work, but essential.
