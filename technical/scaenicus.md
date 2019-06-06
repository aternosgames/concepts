---
description: 'Handles all things global player.'
---

# Scaenicus \(User API\)

[**Scaenicus GitHub Repository**](https://github.com/aternosgames/scaenicus)

## Idea

Scaenicus is an API for user storage, modification, and retrieval. Scaenicus operates through `KeyStone` as a database provider and access api. There are three components: `scaenicus-bukkit`, `scaenicus-bungee`, and `scaenicus-shared`. 

`scaenicus-shared` Contains shared types.

`scaenicus-bukkit` Contains implementations of `scaenicus-shared` and apis for bukkit based extensions. 

`scaenicus-bungee` Contains implementations of `scaenicus-shared` and apis for network-based extensions.

## Features

* Storage, retrieval, and modification apis for:
  * User Ranks
  * User Permissions
  * User Tokens
  * User Level
  * User Statistics
  * User Kits
    * Customized Kits
  * User Preferences (language, ..)
  * User Friends
  * User Punishments
    * Active Punishments
    * Punishment History
  * User Logs
