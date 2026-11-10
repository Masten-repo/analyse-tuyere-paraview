# Analyse thermodynamique d'une tuyère convergente-divergente (ParaView)

Projet de Visualisation scientifique (M1 CHPS, UVSQ – Université Paris-Saclay). Post-traitement avec ParaView des résultats d'une simulation OpenFOAM d'un écoulement compressible dans une tuyère convergente-divergente.

## Pipeline

1. Interpolation Cell Data vers Point Data pour des gradients continus.
2. Calcul du nombre de Mach avec un filtre Calculator (gaz parfait : γ = 1,4, R = 287,05 J·kg⁻¹·K⁻¹).
3. Référentiel géométrique 3D : Extract Surface et Feature Edges à faible opacité.
4. Lignes de courant (Stream Tracer) depuis une source linéaire à l'entrée, volumétrisées avec un filtre Tube et colorées par le Mach.
5. Sonde Plot Over Line sur l'axe de symétrie : pression statique et Mach sur un graphique à double axe.

## Résultat

Le Mach maximal atteint environ 0,3 : l'écoulement reste **subsonique** sur tout le domaine et la tuyère n'est pas amorcée (pas d'ondes de choc, pas d'isosurface M = 1). Le rapport de pression imposé par les conditions aux limites est insuffisant pour atteindre le régime critique au col.

## Rapport

Voir `rapport.pdf`.

## Technologies

ParaView, OpenFOAM (données de simulation)
