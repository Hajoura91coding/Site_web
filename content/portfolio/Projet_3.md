---
date: 2017-04-09T10:58:08-04:00
featured_image: "/images/P3.png"
title: "Anticipation des besoins en consommation électrique de bâtiments"
---
![commentaires](/images/CompetencesP3.PNG "commentaires")

---

Je travaille pour la ville de Seattle qui veut atteindre son objectif de ville neutre en émissions de carbone en 2050.

**Problématique :** Prédire les émissions de C02 et la consommation totale d'énergie de bâtiments

**Missions :**
- Réaliser une courte analyse exploratoire
- Tester différents modèles de prédiction afin de répondre au mieux à la problématique

La ville de Seattle utilise la technique du Benchmarking pour étudier et améliorer les processus pour atteindre l'objectif bas carbone en 2050.

## Nettoyage des données

- Traitement des variables manquantes
- Traitement des variables aberrantes

## Analyse univariée et bivariée

![commentaires](/images/P3_1.png)

- SiteEUIWN (l’énergie totale consommée par m²) présente une distribution décalée à gauche et une queue qui s’étale vers la droite.
- EnergyStarScore (indicateur de performance énergétique) présente une distribution décalée vers la droite et une queue qui s’étale vers la gauche.

![commentaires](/images/P3_2.png)

Le type de bâtiment Campus est celui qui a la plus haute médiane de consommation d’énergie et d’émissions de carbone.
La disparité des boites à moustaches nous indique une corrélation entre la variable BuidingType et les variables émissions de carbone et consommation d'énergie.

## Modélisation

Probléme de machine learning supervisé :
- Identifier les variables sujettes à la fuite de donnée et les traiter
- Traiter les variables catégorielles avec les méthodes "One Hot Encoder" et "Target Encoder"
- Séparer le jeu de donnée en données d'entrainements et de test (80% / 20%)

Voici les modèles implémentés :
- La regression linéaire
- Avec Hyperparamétrage :
  - La regression Ridge et Lasso
  - Random Forest
  - XGboost

XGBoost est le modèle qui présente le meilleur score NMAE (Normalized mean absolute error).

## Conclusion

![commentaires](/images/P3_3.png)
Les résultats sont bons :
- R2 train : 0,85
- R2 test : 0,78

D’après les graphiques, les données sont concentrées entre 13 et 17.

Défaillances :
- Pas mal de valeurs atypiques
- La dispersion des résidus est légèrement inhomogène

---

>***"Exploration détaillée du jeu de données"***

>***"Bonne comparaison des modèles avec des graphiques pertinentes"***

>***"Etude de l'importance des variables"***

>***"Présentation claire et didactique"***

[Link to github repository](https://github.com/Hajoura91coding/Projet_3)
