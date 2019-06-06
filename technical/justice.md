---
description: 'The network element that handles user punishments, and moderation systems.'
---

# Justice \(Punishment and Moderation System\)

[**Justice GitHub Repository**](https://github.com/aternosgames/justice)

## Idea

Justice is the punishment and moderation implementation. It has three components: `justice-bukkit`, `justice-bungee`, and `justice-shared`. Justice operates through `scaenicus` in applying punishments, retrieving permissions, and retrieving user history.

`justice-shared` Contains shared types.

`justice-bukkit` Contains bukkit implementations of `justice-shared`. 

`justice-bungee` Contains bungee implementations of `justice-shared`.

## Features

* Chat filtration 
* Implementations to enforce punishments, such as bans, mutes, kicks.
* Direct user punishment commands for authorized users.
* API For other components to issue and modify punishments.
* ...
