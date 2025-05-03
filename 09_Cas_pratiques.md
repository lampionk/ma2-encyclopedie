# Études de cas – effets complets

### Ex.1 – Pulse RGB
```lua
cmd("BlindEdit On")
cmd("Fixture 1 Thru 10")
cmd("Attribute ColorRGB_R At 100")
cmd("Store Effect 20")
cmd("Assign Effect 20 At Executor 3.201")
cmd("Assign World 1 At Executor 3.201")
cmd("Label Effect 20 \"Pulse Rouge\"")
cmd("BlindEdit Off")
```

### Ex.2 – Blinder Temp
```lua
cmd("BlindEdit On")
cmd("Group 101")
cmd("Attribute Dimmer At 100")
cmd("Store Preset 1.10 /merge")
cmd("Assign Preset 1.10 At Executor 3.110")
cmd("Assign Executor 3.110 /temp")
cmd("Label Executor 3.110 \"Blinder Temp\"")
cmd("BlindEdit Off")
```
