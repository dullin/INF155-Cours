---
title: INF155 - Les tableaux 2D
date: Exercice 7
pandocomatic_:
    use-template: handout
---

Note 1: Dans les exercices qui suivent, vous devez définir une constante de précompilation TAILLE_MAX de valeur 100 qui détermine la taille d'un tableau (sur chacune des dimensions). 

Note 2: Les exercices ci-dessous vous demandent d'écrire des fonctions. Il est entendu que vous devez tester vos fonctions afin d'en valider le fonctionnement (soit depuis votre main, ou mieux, avec une fonction test). Pour faire vos tests, la fonction afficher_tableau2d_int, définie ci-dessous, vous sera très utile. 

~~~c
void afficher_tableau2d_int(int tab2d[TAILLE_MAX][TAILLE_MAX],
                            int nb_lignes, int nb_colonnes) {
    for (int i = 0; i < TAILLE_MAX; ++i) {
        for (int j = 0; j < TAILLE_MAX; ++j) {
            printf("%d ", tab2d[i][j]);
        }
        printf("\n");
    }
}
~~~

# Question 1: 
Écrire une fonction qui calcule la somme des éléments d'un tableau à deux dimensions: 

~~~c
int somme_elements(int tab[][TAILLE_MAX], int nb_lignes, int nb_colonnes);
~~~

# Question 2: 
Écrire une fonction qui calcule la somme des éléments de la diagonale d'une matrice carrée: 

~~~c
int somme_diagonale(int tab[][TAILLE_MAX], int taille_matrice);
~~~

# Question 3:
Écrire une fonction qui compte le nombre d'occurences d'un entier dans un tableau à deux dimensions: 

~~~c
int compter_occurences(int tab[TAILLE_MAX][TAILLE_MAX], int nb_lignes, int nb_colonnes, int a_trouver);
~~~

# Question 4: 
Écrire une fonction qui additionne deux matrices. 

~~~c
void additionner_matrices( 
                double mat1[][TAILLE_MAX], 
                double mat2[][TAILLE_MAX], 
                double resultat[][TAILLE_MAX], 
                int nb_lignes,
                int nb_colonnes); 
~~~

Note: Pour additionner deux matrices, celles-ci doivent avoir les mêmes dimensions.

# Question 5: 
Écrire une fonction qui vérifie si deux matrices sont égales. La fonction renvoie une valeur vraie si elles sont égales, et une valeur fausse sinon.

Note: C'est à vous de déterminer le prototype de la fonction. 

# Question 6: 
Écrire une fonction qui calcule la transposée d'une matrice. Pour rappel, la transposée d'une matrice A correspond à la matrice, notée AT, où les lignes sont converties en colonnes et les colonnes en lignes.

~~~c
void calculer_transposee(double mat[][TAILLE_MAX], double transposee[][TAILLE_MAX], int nb_lignes, int nb_colonnes); 
~~~

# Question 7: 
Écrire une fonction qui reçoit un tableau de points (chaque point est défini par sa coordonnées qui composée d'une abscisse et d'une ordonnée) et qui renvoie la distance minimale entre les points du tableau. Le prototype de la fonction est le suivant : 

~~~c
int distance_minimale(int points[][2], int nb_points); 
~~~