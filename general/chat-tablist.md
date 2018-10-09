# Chat/Tablist

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

