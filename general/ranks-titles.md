# Chat/Levels/Titles

## Chat

### Message

#### Scheme

`LEVEL | NAME: MESSAGE`

#### Example

`42 | Aternos: This is a test message.`

#### Legend

| Variable | Color | Content |
| :--- | :--- | :--- |
| `LEVEL` | Varies by level | Level of the player |
| `NAME` | Blue if member of the AG team, otherwise gray | Name of the player |
| `MESSAGE` | White or gray, whatever is the most readable in terms of foreground-background-contrast and name-message-contrast | Message sent |

### OnHover over Playername

#### Scheme

```text
NAME
TITLE

LEVEL (XP/XP TO NEXT LEVEL)
```

#### Example

```text
Aternos
Legendary Contributor

Level 42 (4000 XP/4150 XP)
```

#### Legend

| Variable | Color | Content |
| :--- | :--- | :--- |
| `NAME` | _See above_ | _See above_ |
| `TITLE` | Varies by title | Title of the player |
| `LEVEL` | _See above_ | _See above_ |
| `XP` | Green | XP of the player |
| `XP TO NEXT LEVEL` | Gray | XP needed for the next level |

## Tablist

### In-Lobby

#### Scheme

`NAME`

#### Example

`Aternos`

#### Legend

| Variable | Color | Content |
| :--- | :--- | :--- |
| `NAME` | _See above_ | _See above_ |

### In-Game

Depends on the gamemode, will be determined later.

## Levels

Levels and the respective amount of XP needed to reach them is calculated through an exponantial term \(That way, players have to gather more XP for the next level\). Rewards aren't pre-defined but rather there is a list of possible rewards for each uprank, which is combined with a multiplier to ensure higher rewards in higher levels. However, special levels might have special rewards, these should be defined here:

| Level | Reward |
| :--- | :--- |
| 42 | _To be determined_ |
| 1337 | _To be determined_ |

## Titles

Titles should be defined here:

| Title | Color \(MC Color Code without prefix\) |
| :--- | :--- |
| ... | ... |

