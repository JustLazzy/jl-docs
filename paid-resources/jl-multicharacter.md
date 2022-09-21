---
description: Multicharacter Script For QBCore
---

# 🚶 JL Multicharacter

### Feature:

* Modern and simple UI
* Support fivem-appearance and qb-clothing ( for showing the ped )
* Developer can set player to have more slots by adding the license.
* Ped support scenario and animdict

### Dependencies:

* qb-core
* qb-spawn
* qb-apartments
* qb-weathersync
* qb-clothing or fivem-appearance

### Installation:

Just remove other multicharacter you have. and replace:

`qb-multicharacter:client:chooseChar` with `jl-multicharacter:client:chooseChar`



### Event:

Client Side:

`jl-multicharacter:client:chooseChar`

Parameter: setwelcome: boolean

Example usage:

```lua
TriggerEvent("jl-multicharacter:client:chooseChar", true)
-- true : show the message landing page (Welcome to xx Server)
```

### Changing the color:

I used svelte to build the UI so that mean you can't change everything on ui side, except for the color, I've used global variable on css, so it may make it easier.

You can use [unminify](https://www.unminify2.com/), to unminify the css. After that don't forget to [minify ](https://www.toptal.com/developers/cssminifier)it again :slight\_smile:.

