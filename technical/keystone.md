---
description: 'The core network element allowing database and inter-component communication and standardization.'
---

# KeyStone \(Core\)

[**KeyStone GitHub Repository**](https://github.com/aternosgames/keystone)

## Idea

Keystone is the centerpiece "keystone" of the network. It contains one component: `keystone-shared`.

`keystone-shared` Serves as an API for other components that implement and create instances of its apis.

## Features

* Database APIs which allow communication with the database through keystone. 
* Standard component enums such as Rank and UserType, that are shared across multiple implementations
* ...
