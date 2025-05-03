# Bonnes pratiques générales

## Programmation MA2 en général
- Toujours travailler sur un **show de test** avant toute mise en production.
- Faire un **`Export Showfile`** avant tout traitement de masse (effets, macros, plugins).
- **Éviter les labels ambigus ou sans nom** : toujours nommer les presets, macros, effects et executors.
- Centraliser les plugins dans une plage dédiée (`Plugin 70 à 99` par exemple).
- Grouper les macros et effects avec un préfixe clair (`Eff_`, `M_`, `GO_`, etc.).

## Scripts & plugins Lua
- Toujours encapsuler la logique dans une fonction `main()` et `return main` à la fin.
- Commencer chaque plugin par `gma.cmd("BlindEdit On")` et finir par `BlindEdit Off`.
- Utiliser `gma.feedback()` pour signaler les étapes majeures (création, assignation, erreur).
- Préférer les `gma.show.getobj.handle()` plutôt que de supposer l'existence d'un objet.
- Respecter la convention `getvar("Nom")` pour lire une variable MA2 (sans `$`).

## Sélection & structure
- Ne **jamais** faire `ClearSelection` avant une boucle `Next`, sinon elle échoue.
- Sauvegarder l’état de la sélection si elle doit être restaurée (`cmd("Store Group TEMP")` / `cmd("Delete Group TEMP")`).
- Pour des traitements par `Next`, structurer le code avec `MatBlocks`, `MatWings` ou `MatInterleave` selon besoin.

## Stockage MA2
- Toujours appliquer `/merge` lors d’un `Store` si risque de perte d’informations.
- Ajouter `/o` (`overwrite`) uniquement quand l’on veut forcer un remplaçant.
- Après un `Store Effect`, il est **fortement recommandé** d’ajouter `Assign Sequence x /Track=Off` dans le cas d’un chaser ou d’un effet multi-pas, afin d’éviter que les cues suivantes héritent des valeurs précédentes. Pour des effets simples ou ponctuels, cela peut ne pas être nécessaire.

## Gestion multi-scripts
- Utiliser `SetVar` et `GetVar` pour partager des valeurs entre plugins sans collision.
- Exemple : `SetVar $Exec_Page_Effect = 3`, puis `getvar("Exec_Page_Effect")`
- Ne jamais stocker directement une valeur fixe si elle est sujette à changement.
