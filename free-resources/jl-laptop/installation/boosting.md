# 🏎 Boosting

Headover to your `qb-core/shared/vehicles` and add this to all your following vehicles

{% hint style="danger" %}
You must add minimum 2 cars per tier to make it work
{% endhint %}

```lua
["tier"] = "D" -- Can either be D, C, B, A, A+, S, S+
```

After that go to your `qb-core/server/player.lua` and add this metadata

```lua
    PlayerData.metadata['carboostrep'] = PlayerData.metadata['carboostrep'] or 0
```
