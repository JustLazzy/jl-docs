# 🖥 General

Go to your `qb-core/server/player.lua` and add this metadata

```lua
    PlayerData.metadata['laptop'] = PlayerData.metadata['laptop'] or {
        background = 'default',
        darkfont = false,
    }
```
