---
date: 2017-04-09T10:58:08-04:00
featured_image: "/images/P1.png"
title: "Conception d'une application au service de la santé publique"
description: "Moteur de recommandation"
---
![commentaires](/images/CompetencesP2.PNG "commentaires")

---

L'agence "Santé publique France" a lancé un appel à projets pour trouver des idées innovantes d’applications en lien avec l'alimentation. Vous souhaitez y participer et proposer une idée d’application.

**Ma mission :**
- Traiter le jeu de données
  - Réfléchir à une idée d'application
  - Repérer des variables pertinentes pour les traitements à venir, et nécessaires pour l'application
  - Nettoyer les données
  - Automatiser ces traitements pour éviter de répéter ces opérations
---

## Mon idée d'application :
**Le système de recommandation basé sur le contenu :**
Méthode basé sur le contenu : l'utilisateur se verra recommander des éléments semblables (au sens d'une mesure de similarité entre éléments) à ceux qu'il a préférés dans le passé.

**Principe de l'application :**
L'utilisateur pourra rentrer un type de plat préparé et choisir le plats selon la notation du nutriscore.

![commentaires](/images/Appli.jpg "commentaires")

**But principal :**
Faciliter le choix des produits aux consommateurs en fonction de leurs besoins grâce aux nutriscores.

**Cible :**
Tous utilisateurs recherchant un produits préparés dans les supermarchés.

## Ciblage des données
![commentaires](/images/choix_plats.png "commentaires")

Mon choix s'est porté pour les composites food (plats préparés) car les classes nutriscore (a, b, c, d, e) sont à peu près équilibrés et aussi pour avoir une certaines logiques d'interprétations

## Réduction dimensionnelle
![commentaires](/images/corrP2.png "commentaires")


Le 1er plan factoriel explique 40.9% de l’inertie totale
- Les fibres, protéines et graisses saturés sont bien représenté
- Les plats préparé avec beaucoup de fibres sont opposé aux plats avec beaucoup de calories et graisses saturées
- Les plats avec des protéines peuvent être « sain » comme « gras »

## Conclusion
Une augmentation du nutriscore revient à une diminution de la qualité nutritionnelle de l'aliments

D’après l’ACP, il y a d’un côté les produits contenant des fibres (des plats préparés « sain ») opposé au plats préparés contenant des graisses saturées (des plats gras).
Normalement, on s’attend a ce que le sel soit opposé au sucre ou les protéines soient opposé au calories mais voici mes interprétations :
- L'ajout de sucre permet un ajustement d’acidité
- L'ajout de sel joue le rôle d'exhausteur de gout
- Ca peut également pallier à la transformation des aliments

## Partie NLP (option : construction du moteur de recommandation)

NLP natural language processing est une branche de l'intelligence artificielle qui a pour but de faire comprendre à la machine le langage humain et de pouvoir l'interpreter.

J'ai pris en compte les textes descriptifs de chaque plats préparés, j'ai nettoyé le texte et j'ai fais une rapide analyse exploratoire.

![commentaires](/images/P2wordcloud.png "commentaires")

Les mots qui reviennent le plus dans les noms des produits sont le boeuf, le fromage et le poulet.

![commentaires](/images/P2wordcloud2.png "commentaires")

Les aliments qui reviennent le plus dans les listes des différents ingrédients de chacun des produits sont : le sel, les enzymes, la sauce soja, l'huile, la farine de blé, l'acide citrique.

La plupart de ces ingrédients ne sont pas bon pour la santé, le sel en trop grande quantité favorise les maladies cardio-vasculaire, l'acide citrique est un additif pour réguler l'acidité et c'est aussi un exhausteur de gout. La sauce soja est ou trop salé ou trop sucré. On trouve également les arôme naturel.

J'applique maintenant la méthode TF-IDF pour faire resortir au mieux les mots clés propres a chaque descriptif de produit et j'applique une distance qui permet de  mesurer la similarité entre deux plats et favoriser la recommandation de plats similaires aux clients.

Voici un exemple de l'application :

![commentaires](/images/recomP2.png "commentaires")



  ---

  >***"Bonne qualité des slides"***

  >***"Bonne présentation de l'idée d'application qui est pertinente et originale"***

  >***"Excellente simulation de l'application avec plusieurs exemples"***

  >***"Très bon travail avec notamment l'utilisation du NLP pour l'application (au delà des attentes, félicitation !)"***

[Link to github repository](https://github.com/Hajoura91coding/Projet_2)
