---
description: 'Customizable, multi-version and easy-to-use game framework built on Glowstone.'
---

# Odessa \(Game framework\)

[**Odessa GitHub Repository**](https://github.com/aternosgames/odessa)

## Idea

Odessa is the foundation for every minigame on Aternos Games. It implements the basic game logic like the game state and player team distribution. Odessa only requires [Playground](playground.md) as dependency and offers an event based API for other components to work with, e.g. integration in the Aternos Games network. 

## Structure

* **`api`**: Interfaces, abstract classes, independent implementations \(only Bukkit\)
* **`core`**: Already implementing some parts of the `api` \(only Bukkit\)
* **`glowstone`**: Supplement missing features of `core` implementations \(using Bukkit and GlowKit\)

## Features

* Game logic
  * Game state/phases
* Arena logic
  * Player spawns
* Team logic
  * Player distribution
  * Colors etc.
* Item distribution
  * Shop system
  * Kits
* Chat formatting
  * Explanations
  * Game specific events \(e.g. Kills\)
* ...

