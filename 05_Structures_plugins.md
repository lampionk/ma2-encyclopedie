# Structures de script recommandées

## Structure de base
```lua
local cmd = gma.cmd
local fbk = gma.feedback

local function main()
  fbk("Début du plugin")
  -- logique ici
  fbk("Fin du plugin")
end

return main
```

## Sections suggérées
1. **Configuration utilisateur** – Variables MA2, `gma.show.getvar()`, valeurs par défaut
2. **Fonctions utilitaires** – Locales : parse, handle, vérification
3. **Logique principale** – Sélection, traitements, assignations
4. **Feedback utilisateur** – Étapes critiques
5. **BlindEdit** – Enclencher pour sécuriser les modifications live
6. **Fin & nettoyage** – ClearAll, restaurer la sélection, confirmation

## Exemple complet
```lua
-- Plugin : Assign Dimmer
local cmd, fbk = gma.cmd, gma.feedback

local function assign_dimmer(group, exec)
  cmd("Assign Group " .. group .. " At Executor " .. exec)
  cmd("Label Executor " .. exec .. " "Dimmer Group " .. group .. """)
end

local function main()
  fbk("Assignation en cours")
  assign_dimmer("101", "3.101")
  fbk("Fait.")
end

return main
```
