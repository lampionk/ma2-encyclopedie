# Snippets utiles

```lua
-- Demande de texte avec valeur par défaut
local input = gma.textinput("Nom du preset", "Blinder")

-- Confirmation utilisateur
if gma.gui.confirm("Tout effacer ?", "Confirmer la suppression") then
  gma.cmd("ClearAll")
end

-- Avancer dans une sélection avec Next
while gma.cmd("Next") do
  gma.feedback("Fixture suivante")
end

-- Appliquer un effet à une sélection
cmd("Assign Effect 5 At Executor 3.105")
```
