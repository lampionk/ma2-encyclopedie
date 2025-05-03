# Transformations d'effets & macros

- **Effet simple vers chaser** : store chaque pas d'effet dans un cue séparé.
- **Effet avec distribution** : utiliser `MatInterleave` ou `MatWings` avant `Store Effect`.
- **Macro vers Executor** : `Assign Macro x At Executor y.z`, puis ajouter options (`Temp`, `GO`, etc.)
- **Effet avec World** : `Assign World 3 At Effect 5` → ne jouera que sur fixtures filtrées.
