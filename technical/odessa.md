---
description: 'Customizable, multi-version and easy-to-use game framework built on Spigot.'
---

# Odessa \(Game framework\)

[**Odessa GitHub Repository**](https://github.com/aternosgames/odessa)

## Idea

Odessa is the foundation for every minigame on Aternos Games. It implements the basic game logic like the game state and player team distribution. Odessa only requires [Playground](playground.md) as dependency and offers an event based API for other components to work with, e.g. integration in the Aternos Games network. 

## Structure

* **`gameapi`**:  Contains the logic to load Odessa Games. Provides the abstract classes, interfaces, and enums for standard games, it also contains the standardized game component types and interfaces. These types are implemented in engine, or in game implementations, or any combination. \(only Bukkit\)
* **`engine`**: Implements some of `api`. Games can create instances of components in `Engine`. For example, it contains a standardized and uniform, lobby system. Other components include services. Services are dependent on `api`, and sometimes other services. The goal of engine is to provide uniform code and systems that most games need. \(only Bukkit\)
## Odessa Features

* Game logic
  * `games.aternos.odessa.gameapi.game.GamePhase` GamePhase: Superclass of all Game phases 
  * `games.aternos.odessa.gameapi.game.GameLifecycleManager` GameLifeCycleManager: Superclass of all GameLifeCycleManagers, (progresses through GamePhase, stores the next phase)
  * `games.aternos.odessa.gameapi.game.GameData` GameData: Superclass of all Game Data, (provides standardized storage for players, spectators, the arena (including spawns), teams).
  * `games.aternos.odessa.gameapi.game.GameConfiguration` GameConfiguration: Superclass of all Game Configuration, (Provides standardized storage of generally constant values, such as player caps, kits, and the game name)
  * `games.aternos.odessa.gameapi.game.Game` Game: Superclass of all Game main classes. Subclasses of Game is registered with the GameApi, contains standardization of the location of a game's implemented GameLifecycleManager, GameData, and GameConfiguration.
* Arena logic
  * `games.aternos.odessa.gameapi.game.element.Arena` Arena: Type for Arenas, contains spawnpoints, the Arena name, and the Arena author(s). 
* Team logic
  * `games.aternos.odessa.gameapi.game.element.Team` Team: Superclass for all team types, contains teamName/id, and the teamColor (can be null)
  * `games.aternos.odessa.gameapi.game.element.IndividualTeam` IndividualTeam: Type for teams containing one player, subclass of Team.
  * `games.aternos.odessa.gameapi.game.element.GroupTeam` GroupTeam: Type for teams containing multiple players, subclass of Team.
* Item distribution
  * Shop system (TBA)
  * `games.aternos.odessa.gameapi.game.element.Kit` Kit: Type for Kits, contains the KitName (may be null), KitItems, and a CoverItem (may be null).
* Chat formatting (TBA)
  * Translations database
  * Explanations
  * Game specific events \(e.g. Kills\)
* Service Components
  * `games.aternos.odessa.engine.service.player.PlayerService` PlayerService: Allows the dispersal of players (#dispersePlayers(Players, Spawns), #dispersePlayers(Arena, Teams), #dispersePlayers(Players, Arena)). Allows giving players kits (#giveKitsToPlayers(Map<Players, Kit>, healPlayers?, cleanPlayers?)) Allows dropping players items (#dropItems(Player, Location, clearPlayer?)). Allows player clearing, and healing.
  * `games.aternos.odessa.engine.service.sidebar.SidebarService` SidebarService: Allows easy creation of player sidebar scoreboards (#createSidebarScoreboard(Player, Sidebar)
    * `games.aternos.odessa.engine.service.sidebar` Sidebar: Type for Sidebars, contains the Board Name, and the Objects of the sidebar as a String list.
  * `games.aternos.odessa.engine.service.ioconfiguration.IoConfigurationService` IoConfigurationService: Allows for the easy creation, writing, and retrieval of custom YAML configurations for things such as spawnpoint/arena configuration.
* `games.aternos.odessa.engine.lobby` Uniform Lobby System: Allows for the creation of uniform lobbies. Initalized with GameLifeCycleManager, so the lobby system can progress the lobby phase (such as when the countdown is completed, and minimum players are met). In addition, it is initalized with the GameApi, and the GameConfiguration, so it can have parameters such as minPlayer, and maxPlayer. The GameLobbySystem hooks into the phase's runnable (LobbyController#lobbyTick()), and registers hooks that are removed when the gamelobbysystem is stopped (LobbyController#removeLobbyListeners()). Contains uniform kit selection, and arena voting systems that use Chest based GUIs, in addition to a uniform sidebar that uses data from the GameConfiguration to populate it. 
