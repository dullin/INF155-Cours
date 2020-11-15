---
title: INF155 - Les chaines
date: Exercice 8
pandocomatic_:
    use-template: handout
---

# Question 0: 
Écrire un programme qui demande à l'usager: 

Son sexe (Masculin ou féminin), 
Son prénom et
Son nom.
Votre programme doit ensuite saluer la personne en ajoutant la salutation (Mme. ou M.). Ex.: "Bonjour M. Bilbo Baggins." 

Note Importante: Votre programme doit afficher un résultat correct si la personne s'appelle (ex.) Johanie Dufour Duquette St Germain.
Question 1: 
Créez un projet pour le laboratoire et ajoutez à votre projet un module que vous nommerez "strutils". Les fonction des questions subséquentes seront ajoutées à ce module. 

# Question 2: 
Écrivez une fonction "str_taille" qui prend une chaine de caractères en paramètre et renvoie sa taille. 

~~~c
int str_taille(const char *chaine); 
~~~

Note importante: Vous devez pas utiliser la fonction "strlen" dans cet exercice.

# Question 3:
Écrivez la fonction str_copie qui lit copie une chaine de caractères source dans une chaine de caractères destination. Votre fonction prends en paramètre un entier taille_max qui représente la taille maximale, en octets, que peut contenir la destination. 

Votre fonction doit renvoyer une valeur vraie si la copie s'est effectuée sans dépassement de capacité, et faux sinon. 

~~~c
int str_copie(char *destination, char *source, int taille_max); 
~~~

Note importante: Vous devez pas utiliser la fonction "strcpy" (ou toute fonction apparentée de la librairie de C) dans cet exercice. 

# Question 4: 
Écrivez la fonction str_comparer qui reçoit deux chaines de caractères str1 et str2, et qui renvoie une valeur nulle si les deux chaines sont identiques, une valeur positive si str1>str2 ou une valeur négative si str1<str2. 

~~~c
int str_comparer(const char *str1,const char *str2);  
~~~

Note: La comparaison doit se faire en vous basant sur le code ASCII des caractères.

Note importante: Vous devez pas utiliser la fonction "strcmp" (ou toute fonction apparentée de la librairie de C) dans cet exercice. 

# Question 5: 
Écrivez la fonction str_concatener qui concatène (i.e. colle à la fin) une chaine de caractères str2 à une chaine de caractères str1. Le résultat doit se trouver dans la chaine str1. Un entier taille_max indique le nombre maximal d'octets que peut contenir str1.

Votre fonction doit renvoyer une valeur vraie si la copie s'est effectuée sans dépassement de capacité, et faux sinon.

~~~c
bool str_concatener(char *str1,const char *str2, int taille_max);
~~~

Note importante: Vous ne devez pas utiliser la fonction "strcat" (ou toute fonction apparentée de la librairie de C) dans cet exercice.

# Question 6: 
Écrivez la fonction "generer_pass" qui génère un mot de passe aléatoire utilisant des lettres (majuscules et minuscules), des chiffres et des symboles. Les symboles que vous utiliserez seront ceux ayant un code ASCII entre 33 et 47. Votre fonction reçoit deux arguments: la chaine de caractère ou stocker le mot de passe, et un entier qui indique la taille du mot de passe (en nombre de caractères) que l'on souhaite obtenir. 

~~~c
void generer_pass(char *dest, int nb_caracteres); 
~~~

Vous devez d'abord créer (au moins) la fonction utilitaire qui vous renvoie une lettre alphabétique aléatoire (Maj ou Min). Cette fonction devrait être réservée au module. 
