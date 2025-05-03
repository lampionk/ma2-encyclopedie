# Encyclopédie MA2 / Lua – Projet Disco

## Table des matières
1. [Bonnes pratiques générales](#bonnes-pratiques-générales)
2. [Erreurs fréquentes & solutions](#erreurs-fréquentes--solutions)
3. [Fonctions Lua utiles](#fonctions-lua-utiles)
4. [Commandes MA2 typiques via gma.cmd()](#commandes-ma2-typiques-via-gmacmd)
5. [Structures de script recommandées](#structures-de-script-recommandées)
6. [Glossaire MA2](#glossaire-ma2)
7. [Snippets utiles](#snippets-utiles)
8. [Transformations d'effets & macros](#transformations-deffets--macros)
9. [Études de cas – effets complets](#études-de-cas--effets-complets)
10. [Fiches de scripts Disco](#fiches-de-scripts-disco)
11. [Annexes – Outils divers](#annexes--outils-divers)
12. [Scripts Chase](#scripts-chase)
13. [grandMA2 Knowledge](#grandma2-knowledge)

---

## grandMA2 Knowledge

### Notions fondamentales
...

### Pièges fréquents
...

### Sélection

- **Ne jamais faire `ClearSelection` juste avant une boucle `Next`** — sinon `Next` n’a rien à faire avancer.
- Faire `ClearSelection` uniquement **avant une sélection manuelle** ou un traitement qui doit reposer sur une sélection fraîche.
- Pour itérer des groupes, utiliser `Group Thru` + `Next` sans perturber la sélection active.
- `MatBlocks`, `MatWings`, `MatInterleave` influent sur le rendu des effets **par pas**.

### Affectation
...

### Macros de contrôle
...

### Layouts
...

### Storage intelligent
...

### Variables & Structure
...
