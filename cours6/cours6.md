---
title: INF155 - Les tableaux
author: Hugo Leblanc
date: Cours 6
pandocomatic_:
    use-template: presentation
    use-template: handout
---

# Tableaux

## Présentation du concept

- Les tableaux sont des collections de plusieurs valeurs du même type sous un seul identificateur.

- Les tableaux nous permettent de travailler avec de grands échantillons de données.

- Pour commencer, nous allons voir seulement les tableaux de tailles statiques. Il existe aussi des tableaux dynamiques.

## Les cases d'un tableau

- Pour distinguer les différentes valeurs à l'intérieur d'un tableau. On utilise un indice qui numérote les cases du tableau.

- L'indice commence toujours à 0. Un tableau de cases aura donc des indices de 0 à 4.

## Déclaration d'un tableau

- Les tableaux sont une extension des variables de bases et se déclarent similairement.

- On ajoute à une déclaration de variables une taille pour indiquer la déclaration d'un tableau et ça taille.

- Nous utiliserons souvent des constantes pour la taille des tableaux.

- Les compilateurs modernes supportent les tableaux statiques de tailles variables. Nous allons nous concentrer sur des tailles fixes jusqu'aux tableaux dynamiques.

~~~c
int notes[8]; //Déclaration d'un tableau de 8 cases.
~~~

## Initialisation des valeurs

- On peut fournir des valeurs initiales à la déclaration d'un tableau.

- L'assignation de plusieurs valeurs en même temps se fait seulement à la déclaration et est impossible autrement.

- On encapsule les assignations entre accolades et elles seront assignées en ordre à partir de la première case.

- Les cases restantes sont initialisées à 0.

~~~c
// Les cases 0, 1 et 2 reçoivent les valeurs
// 23, 65 et 2. La quatrième case est mise à 0.
int tab[4] = {23, 65, 2};
~~~

## Accès aux valeurs du tableau

- L'accès aux valeurs du tableau se fait avec les braquettes carrées.

- On peut utiliser l'accès pour la lecture comme l'assignation.

~~~c
int tab[4] = 34;
printf("%d", tab[4]); // Affiche 34.
~~~

## Exercice

- Écrivez un programme qui déclare un tableau de 100 cases et assigne les 100 premiers termes de la suite de Fibonacci. La suite de Fibonacci se défini de la manière suivante:

~~~c
fibonacci[0] = 0
fibonacci[1] = 1
fibonacci[n] = fibonacci[n - 2] + fibonacci[n - 1]
~~~

# Fonctions et tableau

## Tableau en paramètres d'entrées

- On peut envoyer un tableau comme paramètre d'entrée d'une fonction. On indique un tableau avec ses braquettes carrées.

- La fonction est incapable de déterminer la taille du tableau. Par convention, on utilise habituellement un deuxième paramètre pour indiquer la taille du tableau.

~~~c
int fonction_tab(int tableau[], int nb_elements);
~~~

## Les tableaux sont passés par référence

- Contrairement aux variables, les tableaux sont toujours passés par référence.

- La modification d'un tableau dans une fonction est donc permanente même après l'appel de la fonction.

- Les tableaux sont en fait des pointeurs cachés par une syntaxe spéciale.

# Structures de données

## Description

- Il existe plusieurs manières d'utiliser les tableaux pour regrouper des valeurs.

- Certaines manières sont très communes et sont régies par des conventions spécifiques.

- Nous allons voir une structure de données et ses conventions: les piles.

## Piles

- Le principe est d'empiler des données et de les récupérer à partir du haut de la pile.

- Le type de pile est LIFO (Last In, First Out).

- Les piles sont utilisées pour les applications qui doivent ce souvenir des états précédents.

## Structure de la pile

- Par convention, les piles contiennent 3 informations:
    - La première case contient la taille maximale du tableau.
    - La deuxième case contient un compteur qui pointe sur la tête de la pile.
    - Les restes des cases sont utilisés pour stocker les informations de la pile.

