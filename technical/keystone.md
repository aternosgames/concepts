---
description: 'The core network element allowing database and inter-component communication and standardization.'
---

# KeyStone \(Core\)

[**KeyStone GitHub Repository**](https://github.com/aternosgames/keystone)

## Idea

Keystone is the centerpiece "keystone" of the network. It has three components: `keystone-bukkit`, `keystone-bungee`, and `keystone-shared`.

`keystone-shared` Contains shared types.

`keystone-bukkit` Contains implementations of `keystone-shared` and apis for bukkit based extentions. Also, `keystone-bukkit` communicates with `keystone-bungee` through messaging channels to get information and sync with other components of the network.

`keystone-bungee` Contains implementations of `keystone-shared` and apis for network based extentions.

## Features

* Database APIs which allow communication with the database through keystone. 
* Standard component enums such as Rank and UserType, that are shared across multiple implementations
* ...
