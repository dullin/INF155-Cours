---
title: INF155 - Les tableaux
date: Exercice 6
pandocomatic_:
    use-template: handout
---

# Question 1: 
Écrire un programme où vous: 

Déclarez un tableau de 40 entiers; 
Initialisez toutes les valeurs de votre tableau à 0;
Stockez, dans chaque case de votre tableau, une valeur aléatoire entre 0 et 100.

  


# Question 2: 
Nous souhaitons maintenant créer un sous-programme remplir_aleatoire qui, remplit les cases d'un tableau reçu en paramètre de valeurs aléatoires entre 0 et 100. Votre fonction doit avoir le prototype suivant:  

~~~c
void remplir_aleatoire(int tableau[], int nb_elements); 
~~~

Ensuite, écrivez une fonction test_remplir_aleatoire qui teste votre fonction remplir_aleatoire. La fonction de test doit vérifier le fonctionnement de la fonction testée. Notamment, elle doit tester le fonctionnement normal (il y'a bien des valeurs aléatoires qui sont stockées dans le tableau) ainsi que le fonctionnement aux extrêmes (qu'arrive-t-il si nb_elements=0? si nb_elements<0? si nb_elements=la taille maximale du tableau?). 

La fonction test doit avoir le prototype ci-dessous et renvoyer une valeur vraie si le test s'est bien déroulé, ou fausse sinon. 

~~~c
bool test_remplir_aleatoire(void);
~~~ 

Faites appel à votre fonction test depuis votre main. 




# Question 3:
Écrire une fonctions qui retourne le plus petit élément d'un tableau d'entiers, ainsi que l'indice de ce plus petit élément. Vous devez également écrire la fonction qui effectuera le test de votre sous-programme. 
Nous procéderons en deux étapes:  
- Dans la première étape, nous nous préoccupons uniquement de retourner la plus petite valeur du tableau. Si le tableau est vide, vous devez retourner la valeur de INT_MAX (voir note ci-dessous). Ci-dessous, le prorotype de votre fonction que vous devez écrire, ainsi que la fonction de test correspondante.:  

~~~c
int trouver_plus_petit_element(const int tab[], int nb_elements);
~~~

- Ensuite, modifiez votre fonction et votre fonction de test pour retourner également l'indice du plus petit élément. Compte tenu qu'il n'est pas possible de retourner plus d'une valeur, vous utiliserez un pointeur. Si la plus petite valeur existe plus d'une fois dans la fonction, vous devez retourner l'indice de sa dernière occurence. 
Ci-dessous, le nouveau prototype de la fonction: 

~~~c
int trouver_plus_petit_element(const int tab[], int nb_elements, int *plus_petit_indice);
~~~


Note: La librairie limits.h vous fournit des constantes de précompilation qui vous donnent les valeurs minimales et maximales de chaque type de données de base. Ainsi, la constante INT_MAX vous donne la valeur maxilamale que peut prendre un entier signé. La constante INT_MIN vous donne la plus petite valeurs que peut prendre un entier signé.




# Question 4: 
Écrire une fonction (et la fonction de test correspondante) qui compte le nombre d'occurrences d'un élément dans un tableau.  
Votre fonction doit avoir le prototype suivant: 

~~~c
int compter_occurences(const int tableau[], int nb_el, int el_a_trouver); 
~~~




# Question 5: 
Écrire une fonction (et la fonction de test correspondante) qui recherche un élément dans un tableau. Si l'élément a été trouvé dans le tableau, votre fonction doit retourner l'indice de l'élément. Sinon, votre fonction doit retourner la valeur -1. Si l'élément se trouve plus d'une fois dans le tableau, votre fonction doit renvoyer l'indice de sa première occurrence dans le tableau. 
Pour cette question, vous devez, vous-même, écrire le prototype de la fonction.




# Question 6: 
Écrire une fonction (et sa fonction de test) qui copie un tableau dans un autre. Votre fonction reçoit en argument le tableau source et le tableau de destination, ainsi que les paramètres suivants: 

nb_elts_source: Le nombre d'éléments effectifs du tableau source;
max_elts_dest: La taille du tableau destination (i.e. nombre maximal d'éléments qu'il peut contenir). 
Votre fonction doit d'abord s'assurer que la copie est possible et elle doit renvoyer une valeur vraie si la copie a bien été effectuée, ou une valeur fausse sinon. Si le tableau destination est plus grand que le nombre de cases à copier, vous devez mettre des valeurs nulles dans les cases excédentaires.

Prototype de la fonction:

~~~c
bool copier_tableau(const int tab_source[], int nb_elts_source, int tab_dest[], int max_elts_dest); 
~~~




# Question 7: 
Écrire une fonction, ainsi que la fonction de test correspondante, qui renverse le contenu d'un tableau : le premier élément est échangé avec le dernier, le 2e élément est échangé avec l'avant dernier, etc.

Votre fonction aura le prototype suivant:

~~~c
void renverser_tableau(int tableau[], int nb_elets); 
~~~
