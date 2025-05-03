# Erreurs fréquentes & solutions

| Problème | Symptôme | Solution |
|---------|----------|----------|
| `tonumber(nil)` | Conversion échoue | Vérifier la valeur, prévoir une valeur par défaut |
| `getvar("$Nom")` retourne nil | Mauvais usage de `$` | Utiliser `getvar("Nom")` sans `$` |
| `string.format()` plante | Paramètre `nil` | Encapsuler avec `tostring()` |
| Sélection vide en boucle | `Next` sans effet | Ne pas faire `ClearSelection` juste avant |
| Preset non visible | Pas joué | Appliquer `/Track=Off` sur sequence/effect |
