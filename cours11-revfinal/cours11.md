---
title: INF155 - Révision Final
date: Cours 11
pandocomatic_:
    use-template: handout
---

# Question 1
Écrivez une structure qui représente un étudiant. Les champs seront:

- Une chaine de caractères de 100 cases.
- Un tableau de nombre réelles de 4 cases.

# Question 2
Écrivez une fonction qui reçoit un étudiant et retourne la moyenne de ses 4 examens.

# Question 3
Écrivez une fonction qui reçoit un tableau d'étudiant et sa taille. La fonction retourne la moyenne de la classe. BONUS: Faites la question en n'utilisant pas la fonction fait au numéro précédent.

# Question 4
Écrivez une fonction qui reçoit une chaine de caractère qui représente une nom de fichier, un tableau d'étudiant et sa taille. La fonction ouvre le fichier en mode d'écriture et écrit dans le fichier la moyenne de la classe sur la première ligne et l'information de chaque étudiant sur les lignes suivantes.

~~~
Le fichier texte devrait avoir la forme suivante :
Moyenne : 45.75
Nom : Leblanc 89.6 99.4 100.0 34.6
Nom : Smith 87.54 34.5 45.3 37.8
Nom : Robert 77.7 77.7 77.7 77.7
~~~

# Question 5
Écrivez un fonction qui va lire le fichier précédent et remplir un tableau d'étudiant. La fonction reçoit une chaine de caractères pour le nom de fichier, l'adresse d'un tableau d'étudiant et l'adresse pour la taille du tableau. La fonction doit allouer la mémoire requise pour le tableau d'étudiant avant d'y inscrire les informations.

# Question 6
En assument les structures suivante qui représente un étudiant et une classe avec de l'allocation dynamqique:

~~~c
typedef struct {
    char * nom;
    int taille_nom;
    double * tab_exam;
    int taille_exam;
}t_etudiant_alloc;

typedef struct {
    char * nom_enseignant;
    int taille_chaine;
    t_etudiant_alloc * tab_etudiant[MAX_ETUDIANT];
    int nb_etudiants;
} t_classe;
~~~

# Question 7
Écrivez une fonction qui reçoit l'adresse d'une classe, la taille des chaines de caractères, le nombre d'étudiant et le nombre d'examens de chaque étudiants. La fonction alloue la mémoire de chaque chaine de caractères à la taille voulue. Alloue le tableau d'étudiants et pour chaque étudiant son tableau d'examen.

# Question 8
Écrivez une fonction qui reçoit l'adresse d'une classe et libère la mémoire de tous les éléments alloué dynamiquement dans la structure.

# Question 9
En supposant l’existence des constantes N_LIGNES et N_COLONNES (définies avec #define), écrivez une fonction qui reçoit un tableau de deux dimensions de tailles N_LIGNES par N_COLONNES. La fonction retourne une valeur booléenne qui indique si le tableau est symétrique. Un tableau de deux dimensions est symétrique si la case (i,j) est égale à la case (j,i). On assume que le tableau est carré.