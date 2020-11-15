---
title: INF155 - Les chaines de caractères
date: Cours 8
pandocomatic_:
    use-template: presentation
---

# Table Ascii et le char

- Chaque caractère utilisé dans une chaine est représenté dans la
table de conversion ASCII.

- Le type char permet de contenir un caractère à la fois.

- Un tableau de char pourra donc contenir une chaine de différents caractères.

# Assignation de char

- L'utilisation de l'apostrophe simple est requise pour un unique char.

 ~~~c
 char lettre = 'a';
 ~~~

- Dans la mémoire un nombre est assigné, mais on peut le faire afficher son code ASCII avec l'opérateur de formatage %c.

# Chaine de caractères

- En utilisant un tableau, on peut stocker une chaine de caractères.

- La définition d'une chaine se fait avec les doubles guillemets.

- On peut faire l'assignation d'une chaine à sa déclaration comme un tableau.
~~~c
char mot[100] = "Bonjour la classe";
~~~

- L'affichage de la chaine peut se faire avec l'opérateur de formatage %s dans un printf.

# Le caractère de terminaison NULL

- Chaque chaine de caractères a le nombre zéro comme dernière case dans la chaine.

- Cela indique que la chaine de caractères est terminée.

- Il est donc possible d'avoir de grand tableau pour de petite chaine.

- L'utilisation du caractère de terminaison est automatiquement ajoutée à l'assignation de chaine.

# La saisie de chaine

- Pour saisir une chaine, on peut utiliser scanf mais cela il faut fait attention car on peut facilement dépassé la mémoire du tableau. Le scanf va aussi arrêté au premier espace saisi.

- Nous utiliser fgets pour faire la saisie d'une chaine avec des espaces. Ce dernier permet aussi de limiter le nombre de caractères écrit en mémoire. Par contre, la saisie va contenir le caractère de saut de ligne.

~~~c
char mot[100];
fgets(mot, 100 ,stdin);
~~~

# Caractère d'échapement

# Libraire string.h

- strlen(str) - Retroune le nombre de caractères de la chaine.

- strcopy(dest, source) - Copie une chaine dans une autre.

- strncopy(dest, source, n) - Copie de la chaine dans une autre avec un nombre de caractères maximal.

- strcat(dest, source) - Concatène(colle) la source à la fin de la destination.

- strcmp(str1, str2) - Compare deux chaines voir si elles sont identiques. Retourne 0 si elles le sont.

- atoi(str) - Convertis une chaine en entité numérique.
