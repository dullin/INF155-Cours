---
title: INF155 - Les tableaux 2D et les pointeurs
date: Cours 7
pandocomatic_:
    use-template: presentation
---

# Tableaux

## Les tableaux et les pointeurs

- L'utilisation de pointeurs est utilisée dans les tableaux.

- L'identificateur est utilisé comme adresse de base du tableau.

- L'indice est ensuite utilisé pour savoir le nombre de "sauts" à faire pour arriver à la valeur voulue.

- `tab[i]` et `*(tab+i)` représente la même sélection de valeur.

## Les tableaux de deux dimensions

- La création de tableaux de deux dimensions demande d'assigner les deux dimensions à la déclaration. `tab2d[5][5]`

- Les indices de tableaux sont représentés comme une paire (ligne, colonne).

- Le tableau est stocké en mémoire de manière continue ligne par ligne.

## Utilisation de tableaux 2D

- L'assignation de valeur se fait avec des accolades imbriquées à la déclaration. `{ {1, 2, 3}, {4, 5, 6} }`

- L'utilisation de tableau 2D requiert de donner de nombre de colonnes au prototype de fonction.

~~~c
int ma_fonction(int tab[][10], int nb_lignes, int_nb_colonnes);
~~~

# Les modules

## Séparation d'un programme en module

- Nos programmes sont déjà séparés en fonctions. La prochaine étape est de séparer les fonctions en modules dans des fichiers distincts.

- Chaque module aura une paire de fichiers. Un fichier d'en-tête (.h) et un fichier source (.c).

- Nos programmes seront donc plus modulaires par rapport à leur différent contexte.

## Fichiers d'en-tête (.h)

- Le module d'en-tête représente "l'interface" à notre module.

- Il contient les déclarations de fonctions, les modules requis et les constantes offertes.

- Les fichiers d'en-tête contiennent des protections de préprocesseur pour ne pas être inclus plusieurs fois.

- Les en-têtes de fonctions seront dans le fichier d'en-tête.

## Fichier de source (.c)

- Le module source représente "l'implémentation" de notre module.

- Il contient les définitions de fonctions et autres déclarations privées au module.

