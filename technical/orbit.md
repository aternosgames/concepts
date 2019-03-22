---
description: 'HTTP API to provide on demand and realtime access to the database.'
---

# Orbit \(Database\)

[**Orbit GitHub Repository**](https://github.com/aternosgames/orbit)

## Idea

The central database is not directly accessable by any other component. Components like
the gameserver integration, the matchmaking service, the bungeecord integration or the website all 
communicate with Orbit, which provides a central HTTP API to add, modify, access and
delete database entries. It authorizes the client and restricts database access. Additionally,
it can perform basic processing of the data before or after storing it in the database, e.g.
calculating the level based on XP. Orbit includes two different methods to access the data: REST-like
HTTP requests or websocket based realtime communication.

## Technology

To implement these features easily the database backend could be [RethinkDB](https://www.rethinkdb.com/) and
Orbit could be written in [NodeJS](https://nodejs.org/en/).

## Features

* REST API
* Websocket API
* Authorization
* Access control
* Middleware/Processing

## Data

* User/Player
  * User Rank
  * User Preferred Language
  * User Currency (Such as gold to buy kits won in games, etc)
  * User Punishments
    * Past Punishments
    * Active Punishments
  * Personal Statistics  
    * Player Game Wins (stored/received by game or total)
    * Player Kills (stored/received by game or total)
    * Player Deaths (stored/received by game or total)
  * User Game Data Storage
    * Owned Kits
  * User Level
* Chat (Friends/Party)
* Statistics
  * Storage for overall network statistics
    * Amount of played games...etc.
* ...
