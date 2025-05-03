# Commandes MA2 typiques via gma.cmd()

```lua
gma.cmd("BlindEdit On")
gma.cmd("Store Executor 3.101")
gma.cmd("Assign Preset 4.1 At Cue 2")
gma.cmd("Label Effect 7 \"Strobe Rouge\"")
gma.cmd("SetVar $DimGroup = \"101 Thru 110\"")
```

- Toujours échapper les guillemets dans les `Label` et `TextInput`.
- `Store Effect x /o` : overwrite, `Store ... /merge` : conserver, `Assign ... /Track=Off` : obligatoire après effet.
