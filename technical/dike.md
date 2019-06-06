---
description: 'The network element that handles user punishments, and moderation systems.'
---

# Dike \(Punishment and Moderation System\)

[**Dike GitHub Repository**](https://github.com/aternosgames/dike)

## Idea

Dike is the punishment and moderation implementation. It has three components: `dike-bukkit`, `dike-bungee`, and `dike-shared`. Dike operates through `scaenicus` in applying punishments, retrieving permissions, and retrieving user history.

`dike-shared` Contains shared types.

`dike-bukkit` Contains bukkit implementations of `dike-shared`. 

`dike-bungee` Contains bungee implementations of `dike-shared`.

## Features

* Chat filtration 
* Implementations to enforce punishments, such as bans, mutes, kicks.
* Direct user punishment commands for authorized users.
* API For other components to issue and modify punishments.
* ...
