# Fonctions Lua utiles

```lua
-- Vérifie l’existence d’un preset
gma.show.getobj.handle("Preset 4.1") ~= nil

-- Boucle sur une chaîne du type "1 Thru 5 + 8"
function parseNumberList(str)
  local res = {}
  for part in str:gmatch("[^+]+") do
    local a, b = part:match("(%d+)%s*Thru%s*(%d+)")
    if a then
      for i = tonumber(a), tonumber(b) do table.insert(res, i) end
    else
      table.insert(res, tonumber(part))
    end
  end
  return res
end
```
