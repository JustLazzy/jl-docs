---
description: Configure the target
---

# Target

On version <mark style="color:blue;">1.0.1</mark> you can configure your target for each motel.

`Default Config`

```lua
Config.Target = {
    stash = false,
    logout = true,
    outfit = false
}
```

`Motel Config` you can set the target per motel or it'll use the default config above

```lua
Target = {
    stash  = false,
    logout = true,
    outfit = false
},
```

#### Icon

```lua
Config.Icon = {
    stash = 'fas fa-briefcase',
    outfit = 'fas fa-tshirt',
    logout = 'fas fa-user',
    rent = 'fas fa-home',
    renew = 'fas fa-home',
    reclaim = 'fas fa-key',
    reset = 'fas fa-key',
    cancel = 'fas fa-ban'
}
```

You can change the icon as you need with [fontawesome](https://fontawesome.com/)
