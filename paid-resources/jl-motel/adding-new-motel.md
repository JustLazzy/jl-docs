# Adding new motel

Here's how you add new motel

{% hint style="warning" %}
**Warning:**

Please read carefully, so you don't have error after adding new motel, make sure you don't have any syntax error, or forgot to put a `" , "` on your config file
{% endhint %}

## Non MLO

Here's some example to do that.

```lua
   ['cool_motel'] = {
        label = "Motel Name",
        rent = {
            coords = vector4(290.25, -268.96, 54.0, 338.77) -- rent coords, must be vector 4, this is where the guy stand
        },
        price = 10, -- Motel prices
        motel = {
            ["cool:1"] = { --motel index [MUST BE UNIQUE]
                enter = vector4(286.91, -266.79, 54.0, 339.62), -- coords where you enter the motel
                label = "Cool 1", -- Motel label, example Pinkcage 1 that mean Pinkcage room 1
                locked = true, -- Don't touch it
                owned = false, -- Don't touch it
            },
        }
    }
```

## MLO

For this one you need more effort

Here's some example

```lua
['pinkcage'] = {
        label = "Pinkcage",
        mlo = true, -- You need to set this to true if you use mlo
        rent = {
            coords = vector4(325.03, -229.67, 54.22, 155.9) -- Coords where the guy stand
        },
        price = 110,
        motel = {
            ["pinkcage:1"] = { -- motel index, must be unique, and same with doorlock id
                enter = vec3(306.848938, -213.674500, 54.371540), -- door coords, you can take it on your doorlock config
                locked = true, -- Don't touch it
                label = "Pinkcage 1", -- Your motel label
                owned = false, -- Don't touch it
                logout = { -- This is where you can logout your character (with target)
                    coords = vector3(303.58, -209.14, 54.27), 
                    width = 0.4,
                    height = 0.4,
                    name = "pinkcage:1:logout",
                    heading = 334,
                    minZ=53.92,
                    maxZ=54.32
                },
                stash = { -- Where you can open your stash (PolyZone)
                    coords = vector3(306.87, -208.27, 54.23),
                    width = 1.6,
                    height = 1.8,
                    name = "pinkcage:1:stash",
                    heading=339,
                    minZ=50.43,
                    maxZ=54.63
                },
                outfit = { -- Where you can open your outfit (PolyZone)
                    coords = vector3(302.43, -206.77, 54.23),
                    width = 1.8,
                    height = 1.4,
                    name = "pinkcage:1:outfit",
                    heading=339,
                    minZ=53.18,
                    maxZ=55.38
                },
            },
}
```

### Explanation

{% hint style="info" %}
Make sure your doorlock id and motel index are the same
{% endhint %}

Example:

Your doorlock config are like this

```javascript
Config.DoorList['pinkcage:1'] = {
    distance = 2,
    locked = true,
    objCoords = vec3(306.848938, -213.674500, 54.371540),
    objName = -1156992775,
    objYaw = 68.909614562988,
    fixText = false,
    pickable = true,
    audioRemote = false,
    doorType = 'door',
    doorRate = 1.0,
    --audioLock = {['file'] = 'metal-locker.ogg', ['volume'] = 0.6},
    --audioUnlock = {['file'] = 'metallic-creak.ogg', ['volume'] = 0.7},
    --autoLock = 1000,
}
```

`pinkcage:1` is the id of your doorlock so your motel room config should be like this

```javascript
["pinkcage:1"] = {
                enter = vec3(306.848938, -213.674500, 54.371540),
                locked = true,
                label = "Pinkcage 1",
                owned = false,
                logout = {
                    coords = vector3(303.58, -209.14, 54.27),
                    width = 0.4,
                    height = 0.4,
                    name = "pinkcage:1:logout",
                    heading = 334,
                    minZ=53.92,
                    maxZ=54.32
                },
                stash = {
                    coords = vector3(306.87, -208.27, 54.23),
                    width = 1.6,
                    height = 1.8,
                    name = "pinkcage:1:stash",
                    heading=339,
                    minZ=50.43,
                    maxZ=54.63
                },
                outfit = {
                    coords = vector3(302.43, -206.77, 54.23),
                    width = 1.8,
                    height = 1.4,
                    name = "pinkcage:1:outfit",
                    heading=339,
                    minZ=53.18,
                    maxZ=55.38
                },
            },
```

enter coords must be the same as your objCoords



#### Stash, Logout, Outfit

These 3 config uses polyzone. You can use `/pzcreate box`  after you configure the position and size. You should have this format of config

```lua
BoxZone:Create(vector3(306.87, -208.27, 54.23), 1.6, 1.8, {
  name="pinkcage:1:stash",
  heading=339,
  --debugPoly=true,
  minZ=50.43,
  maxZ=54.63
})
```

After that, you can configure your stash to this format

```lua
stash = {
    coords = vector3(306.87, -208.27, 54.23),
    width = 1.6,
    height = 1.8,
    name = "pinkcage:1:stash",
    heading=339,
    minZ=50.43,
    maxZ=54.63
},
```
