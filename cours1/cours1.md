% INF155 - Fondements
% Hugo Leblanc
% Cours 1

# Présentation du cours

## Présentation personnelle
Hugo Leblanc

hugo.leblanc@etsmtl.ca

Baccalauréat en génie électrique de l’ÉTS en 2012

Programmeur depuis 1996

Spécialisation en systèmes embarqués

## Plan de cours
- Pondération
- Date de remise
- Politique de plagiat

## Moodle ena.etsmtl.ca
- Centre de toutes les interactions du cours
- Notes de cours, exercices, remises

## Slack
- Plate-forme de communication à l'extérieur du cours

## Structure de travail du cours
- 1000 erreurs à faire avant la fin de la session
- Très facile de perdre le contrôle sur la matière
- Les travaux pratiques sont des préparations aux examens

# Programme informatique

## Description
Un programme est une suite d'instructions écrites pour être exécutées par un ordinateur. Le programme est habituellement écrit initialement sous forme de **code source**. Pour le langage C, le **code source** est ensuite compilé par un **compilateur** qui transforme le code source en code binaire qui pourra être **exécuté** par un ordinateur.

## Code source
La majorité du temps d'un programmeur est utilisé pour écrire le code source d'un programme. Le programme est basé sur 3 concepts fondamentaux:

- Instructions
- Mémoire
- Exécution séquentielle

## Édition du code source
Un éditeur de code source peut être n'importe quel éditeur de texte. Pour faciliter les autres étapes de la création d'un programme, nous utiliserons des IDE (Integrated development environment) qui facilitent l'édition, la compilation et l'exécution de nos programmes.

# Notre premier programme

## Éléments de base d'un programme en C
~~~~c
int main(void){
    return 0;
}
~~~~

Notre premier programme contient seulement les éléments primordiaux pour l'exécution de programme.

## Commentaires
Les commentaires dans le code source sont du texte laissé pour un autre être humain. L'ordinateur fait fit des commentaires à la compilation et l'exécution du programme.

Les commentaires restent **primordiaux** à la programmation, car ils permettent d'apporter des précisions aux instructions qui ne sont pas nécessairement claires.

##
Les commentaires sont présentés de deux façons:

- "//" commente le texte jusqu'à la fin de la ligne courante
- "/*" et "*/" permet de délimiter un bloc de commentaire sur plusieurs lignes.

## Où mettre des commentaires
- En-tête de fichiers
- Description de fonctions
- À l'intérieur de nos instructions pour décrire nos actions
- **NE PAS** reformuler l'instruction en commentaire

## Notre premier programme avec commentaire
~~~~c
/*
Notre premier programme. Il ne fait rien.

Hugo Leblanc
*/

// La fonction main est obligatoire et le point d'entrée.
int main(void){
    // Permet de communiquer la fin du programme.
    return 0;
}
~~~~

# Instructions

##
Les instructions servent à produire la séquence d'événements du programme. La majorité des instructions doivent être contenues à l'intérieur de fonctions. Les instructions d'un programme C sont exécutées de manières séquentielles à partir du point d'entrée (la fonction main).

En C, les instructions sont toujours terminées par le **point-virgule** ";".

## Expressions
Plusieurs instructions utilisent les expressions comme élément. Une expression est une opération qui est **évaluée** pour **retourner** une valeur. Les expressions sont évaluées selon la priorité des opérateurs.

##

Nous connaissons d’amblé déjà deux types d'expressions:

- Les expressions littérales d'une valeur. 8 ou 12 par exemple.
- Les expressions arithmétiques mathématiques. 2 + 5 retourne 7.

Tenez compte que si un élément demande une expression, n'importe quelle expression valide pourra être utilisée.

##

~~~~c
int main(void){
    4 + 2;
    return 0;
}
~~~~

# Variables

## Description
Une variable est la combinaison de:
- Un espace mémoire réservé avec une valeur assignée
- Un identificateur
- Un type

## Espace mémoire
Pour faire l'utilisation d'une variable, celle-ci doit être déclarée et donc avoir une place réservée dans la mémoire de l'ordinateur avant qu'elle puisse être utilisée. Nous reviendrons plus en détail sur les concepts de l'utilisation de la mémoire.

## Identificateur
L'identificateur est le "nom" de la variable, c'est avec l'identificateur qu'on va retrouver le bon espace mémoire pour retrouver la valeur à sauvegarder.

## Règles de l'identificateur
- Peut seulement contenir des lettres alphabétiques non accentuées, des chiffres ou le tiret-bas "_"
- Le premier caractère doit être une lettre alphabétique
- Ne peut pas être un mot réservé du C
- Faire attention, les casses majuscule et minuscule sont considérées comme des caractères différents

## Type
Le type de la variable permet de définir le genre de donnée que la variable peut contenir. Le type va limiter les valeurs possibles que la variable peut stocker.

## Type entier
type      |  taille   |   signed | unsigned
-------   |  ---------| ---------|--------
bool      |  1 bit    |   0 → 1  | Non défini
char      |  1 octet  |   -128 → 127 |0 → 255
short     |  2 octets |   -32768 → 32767 | 0 → 65535
int       |  4 octets |   -2 147 483 648 → 2 147 483 647 | 0 → 4 294 967 296
long      |  4 octets |   -2 147 483 648 → 2 147 483 647 |0 → 4 294 967 296
long long |  8 octets | -9.2 x 10<sup>18</sup> → 9.2 x 10<sup>18</sup> |0 → 1.8 x 10<sup>19</sup>

## Type réel
type | taille | Valeurs
---- | -------|--------
float | 4 octets | 1.175494351 x 10<sup>-38</sup> → 3.402823466 x 10<sup>38</sup>
double | 8 octets | 2.2250738585072014 x 10<sup>-308</sup> → 1.7976931348623158 x 10<sup>308</sup>
long double | 8 octets | 2.2250738585072014 x 10<sup>-308</sup> → 1.7976931348623158 x 10<sup>308</sup>

## Type caractère
Le type char est utilisé pour représenter un caractère. Nous verrons l'utilisation en détail de char quand nous étudierons les chaînes de caractères.

Pour l'instant, suffit de savoir que les chaînes de caractères sont représentées sous des doubles guillemets "" dans le langage C.

## Déclaration d'une variable
La syntaxe générale d'une déclaration est :

~~~c
type identificateur [= valeur_initiale];

//Exemples de déclarations
int nb_etudiants;
double prix = 2.178;
~~~

Si la valeur initiale n'est pas fournie, une valeur nulle par défaut est assignée.

Les déclarations de variables se font au début du bloc de code dans lequel les variables seront utilisées.

## Assignation d'une variable
L'assignation est l'instruction utilisée pour changer la valeur d'une variable. La syntaxe est la suivante:

~~~~c
variable = expression;

//Exemples d'assignations
//On assume que les variables sont déjà déclarées.
nb_etudiants = 27;
prix = 13 + 45.3;
~~~~

L'opérateur "=" est utilisé pour l'assignation. Faire attention, l'assignation se fait toujours **de la droite vers la gauche**.

## Utilisation d'une variable dans une expression
Une fois la variable déclarée, elle peut être utilisée dans n'importe quelle expression de notre programme. L'utilisation de la variable sera remplacée par sa valeur en mémoire au moment de l'exécution.

Faire attention à l'exécution séquentielle du programme. La valeur dans la variable peut changer durant l'exécution.

## Exemple d'utilisation de variable dans un programme
~~~~c
int main(void){
    int x = 5;
    int y;
    int z;

    y = 4;
    y = x + 12;
    z = x + y;
    x = x + z;
    return 0;
}
~~~~

À la fin de l'exécution de se programme, quel sera les valeurs dans x, y et z?

## Conversion de type
Si la valeur à assigner dans une variable n'est pas du bon type, il y aura une conversion de type. La conversion peut être implicite ou explicite.

La conversion implicite se fait automatiquement. La conversion explicite demande une syntaxe spéciale:

~~~c
variable = (nouveau_type)expression;
// Exemple
int nb_etudiants;
nb_etudiants = (int)(14 / 3);
~~~

# L'affichage et la saisie

##
L'affichage et la saisie de données nous permettent d'interagir avec nos programmes exécutés. L'affichage va nous permettre d'afficher de l'information à l'écran et la saisie nous permet d’entrer de l'information durant l'exécution du programme. Cette fonctionnalité nous est fournie sous forme de fonctions déjà existantes.

## Commandes de préprocesseur
Pour utiliser les fonctions d'affiche et de saisies, on doit importer leur déclaration avec une commande de préprocesseur. Le préprocesseur permet de faire une gestion préliminaire du code avant d'être compilé. Dans notre cas, il permet d'importer la librairie stdio qui contient les fonctions printf et scanf pour l'affichage et la saisie respectivement.

## Exemple d'importation de librairies avec le préprocesseur
Les commandes de préprocesseur commencent toujours par le "#". Pour inclure une librairie, on utilise la commande include suivie du nom de la librairie voulue. Le nom de la librairie sera entre crochets suivi de l'extension .h.

~~~~c
#include <stdio.h>
~~~~

Il existe d'autres commandes de préprocesseur et même d'autres manières d'utiliser le include mais nous les verrons plus tard.

## La fonction printf
La fonction permet de base d'afficher un message sous forme de chaîne de caractères à l'utilisateur durant l'exécution de son programme.

printf permet aussi d'avoir des opérateurs de formatage pour inclure des données de manière dynamique durant l'exécution. Cela est utile pour afficher les valeurs d'une variable par exemple.

## Exemple d'utilisation de printf
~~~c
#include <stdio.h>

int main(void){
    int x = 5;
    printf("Un premier affichage!\n");
    printf("Affichage d'une valeur : %d \n", x);
    printf("L'utilisation est une expression : %d \n", 4 + 2);
}
~~~

## Opérateurs de formatage de base
Types | Format
------|-------
char | %c
int | %d ou %i
unsigned int | %u
long int | %ld ou li
unsigned long int | %lu
float | %f
double | %lf

## Caractères d'échappement
Certains caractères et symboles sont impossibles à écrire et nécessitent un caractère d'échappement pour que printf puisse l'interpréter correctement.

##
Voici quelques caractères d'échappements utiles:

Séquence | Utilisation
-------| -----
\\n | Saut de ligne
\\t | Tabulation horizontale
\\\\ | Affiche le symbole \\
\\" | Affiche le symbole "
\\' | Affiche le symbole '

## La fonction scanf
La fonction scanf fait la saisie d'une valeur à l'exécution du programme. Le programme s'arrête pour faire la saisie au clavier de la valeur. La valeur saisie est assignée dans une variable. La syntaxe d'utilisation est :

~~~c
scanf("format_lire", &variable);
// Exemple
int x;
scanf("%d", &x);
~~~

L'utilisation du **&** est très importante. Nous verrons ses implications plus tard.

# Les opérateurs

## Opérateurs mathématiques
Opérateur | Exemple | Résultat
----|----|----
* | x * y | Multiplication de x par y
/ | x / y | Division de x par y
% | x % y | Modulo de x par y
+ | x + y | Addition de x par y
- | x - y | Soustraction de x par y
++ | ++x ou x++ | Incrémentation préfixe ou post-fixe
-- | --x ou x-- | Décrémentation préfixe ou post-fixe


## Opérateurs relationnels
Les opérateurs relationnels permettent de comparer deux valeurs numériques.

Opérateur | Exemple | Résultat
----|----|----
< | x < y | Vrai si x est inférieur à y
> | x > y | Vrai si x est supérieur à y
<= | x <= y | Vrai si x est inférieur ou égal à y
>= | x >= y | Vrai si x est supérieur ou égal à y
== | x == y | Vrai si x est égal à y
!= | x != y | Vrai si x est différent à y

# Structure de contrôle conditionnelle - if

## Description
Les structures de contrôle permettent de ne pas suivre le flot d'exécution normale d'un programme.

La structure conditionnelle permet de sauter par dessus des bouts de code selon une condition donnée.

La condition est considérée comme une expression booléenne. La valeur 0 est considérée comme fausse, le reste est vrai.

## Syntaxe

~~~c
if (condition) {
    //Instruction
}
// Exemple
if (x > 4) {
    printf("Dans le if!");
}
~~~
