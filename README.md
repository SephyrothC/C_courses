![banner](https://github.com/fareanor3/C_courses/blob/5e58730c84283c11864b52350b6233b3947dafa7/banner.jpg)
# C_courses

##  Mind the openclassroom courses

___

> Card on the C language from the [Open Classroom](https://github.com/fareanor3/C_courses/blob/e5c10bb83f72568782022b9df525565999583c23/banner.jpg) course . 

___

####  Code minimaliste :

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
  printf("Bonjour");
  return 0;
}
```

|'But'|*Fonction*|
| :--------: |:-----:|
| `affichage`  |   printf("Bonjour")  |
|`entée utilisateur`|scanf("%d", &age)|
|`retour à la ligne (= « Entrée »)` | \n |
|`tabulation`|\t|
|`commentaire`|//|
|`debut & fin commentaire`|/* & *\|


#### Variable :

|'Nom du type'|*Min*|*Max*|
| :--------: |:-----:|:-----:|
|'signed char'|-127|127|
|'int'|-32 767|32767|
|'long'|-2 147 483 647|2 147 483 647|
|'float'|-1 x1037|1 x1037|
|'double'|-1 x1037|1 x1037|

> Généralement on utilise pour un nombre entier : ```int``` et pour un flottant un ```double```

#### ❗ Attention : 
> Les trois premiers types (```signed char```,```int```,```long```) permettent de stocker des nombres entiers :
Les deux derniers (```float```,```double```) permettent de stocker des nombres décimaux (appelés nombres flottants) : 13.8, 16.911…

> ```unsigned``` est un mot clée permetant de stoquer que des nombre possitif 
```const``` pour déclarer une constante

#### Afficher le contenu d'une variable :

```c
printf("il vous reste %d vies et vous etes au niveau", nombre_de_vies, niveau);
```

|'Format'|*Type attendu*|
| :--------: |:-----:|
|`%d`|int|
|`%ld`|long|
|`%f`|float|
|`%f`|double|

|'Operation'|*Signe*|
| :--------: |:-----:|
|`Addition`|+|
|`Soustraction`|-|
|`Multiplication`|*|
|`Division`|/|
|`Modulo`|%|

#### Incremetation

```C
nombre ++ ;
nombre += 4;
nombre -= 3;
nombre *= 5;
nombre /= 3;
nombre %= 3;
```

### La bibliothèque mathématique

``` c
#include <maths.h>
```

#### ❗ Attention tous est en ```bouble```

|'But'|*Fonction*|
| :--------: |:-----:|
|`valeur absolue`|fabs(value)|
|`valeur entière du dessus`|ceil(value)|
|`valeur entière du dessous`|floor(value)|
|`puissance`|pow(number,puissance)|
|`racine carrée`|sqrt(number)|
|`sin`|sin(radian)|
|`cos`|cos(radian)|
|`tan`|tan(radian)|
|`asin`|asin(radian)|
|`acos`|acos(radian)|
|`atan`|atan(radian)|
|`exponetiel`|exp(number)|
|`log`|log(number)|
|`ln`|ln(number)|
|`log10`|log10(number)|

#### symbole a connaitre

|*Signification*|'Symbole'|
| :--------: |:-----:|
|`est égal à `|==|
|`supperieur`|>|
|`inferieur`|<|
|`suprerieur ou egal`|>=|
|`inférieur ou égal`|<=|
|`est different de`|!=|

### Conditions : 
#### if : 

```C
if (/* Votre condition */)
{
  // Instructions à exécuter si la condition est vraie
}
```

#### else :

```C
if (age >= 18) // Si l'âge est supérieur ou égal à 18
{
  printf ("Vous etes majeur !");
}
else // Sinon...
{
  printf ("Ah c'est bete, vous etes mineur !");
}
```

#### else if:

```c
if (age >= 18) // Si l'âge est supérieur ou égal à 18
{
  printf ("Vous etes majeur !");
}
else if ( age > 4 ) // Sinon, si l'âge est au moins supérieur à 4 
{
  printf ("Bon t'es pas trop jeune quand meme...");
}
else // Sinon...
{
  printf ("Aga gaa aga gaaa"); // Langage bébé, vous pouvez pas comprendre
}
```

#### plusieur condition a la fois

|*Signification*|'Symbole'|
| :--------: |:-----:|
|`ET`|`&&`|
|`OU`|`||`|
|`NON`|`!`|

#### Exemple :

```c
if (age > 18 && age < 25);
if (age > 30 || argent > 100000);
if (!(age < 18));
```

#### Bouléen :

```c
if (1)
{
    printf("C'est vrai");
}
else
{
    printf("C'est faux");
}
```

#### Switch:

```c
switch (age)
{
case 2:
  printf("Salut bebe !");
  break;
case 6:
  printf("Salut gamin !");
  break;
case 12:
  printf("Salut jeune !");
  break;
case 16:
  printf("Salut ado !");
  break;
case 18:
  printf("Salut adulte !");
  break;
case 68:
  printf("Salut papy !");
  break;
default:
  printf("Je n'ai aucune phrase de prete pour ton age  ");
  break;
}
```

#### La boucle while

```c
while (/* Condition */) // (1) pour une boucle infini
{
    // Instructions à répéter
}
```

#### La boucle do while ( pour boucler au moins une fois )

```c
int compteur = 0;

do
{
    printf("Salut les Zeros !\n");
    compteur++;
} while (compteur < 10);
```

#### La boucle for

```c
int compteur;

for (compteur = 0 ; compteur < 10 ; compteur++)
{
  printf("Salut les Zeros !\n");
}
```

#### Tirer un nomnbre au hasard

```c
// ajouter
#include <time.h>

const int MAX = 100, MIN = 1;

srand(time(NULL)); // strand() inicialise le compteur de nombre aléatoire
nombreMystere = (rand() % (MAX - MIN + 1)) + MIN; //rand() génère un nombre au hasard entre 1 et 100
```

### Les fonctions

#### schéma d'une fonction
```c
type nomFonction(parametres)
{
    // Insérez vos instructions ici
}
```

#### code menu
```c
int menu()
{
    int choix = 0;
    while (choix < 1 || choix > 4)
    {
        printf("Menu :\n");
        printf("1 : Poulet de dinde aux escargots rotis a la sauce bearnaise\n");
        printf("2 : Concombres sucres a la sauce de myrtilles enrobee de chocolat\n");
        scanf("%d", &choix);
    }    
    return choix;
}    
int main(int argc, char *argv[])
{    
    switch (menu()) \\ récupère directement le choix utilisateur
    {
        case 1:
            printf("Vous avez pris le poulet\n");
            break;
        case 2:
            printf("Vous avez pris les concombres\n");
            break;  
    return 0;
}
```

### La programmation modulaire

> A chaque fois que vous faites appel à une fonction X dans un fichier, il faut que vous ayez inclus les prototypes de cette fonction dans votre fichier. Cela permet au compilateur de vérifier si vous l'avez correctement appelée.
> Quand dans votre code vous faites appel à une fonction, votre ordinateur doit déjà la connaître, savoir combien de paramètres elle prend, etc.

#### ❗ Attention : 

On met rarement les headers avec les fichiers c. 

#### Les signes

> Les chevrons< > pour inclure un fichier se trouvant dans le répertoire « include » de votre IDE ;
> Les guillemets" " pour inclure un fichier se trouvant dans le répertoire de votre projet (à côté des.c, généralement).

#### Dans le fichier C

```c
#include <stdlib.h>
#include <stdio.h>
#include "jeu.h"

void jouer(SDL_Surface* ecran)
{
// ...
```
#### Dans le fichier H
```h
    void jouer(SDL_Surface* ecran);
    void deplacerJoueur(int carte[][NB_BLOCS_HAUTEUR], SDL_Rect *pos, int direction);
    void deplacerCaisse(int *premiereCase, int *secondeCase);
```

#### La compilation séparée

![Diagrame de compilation](https://github.com/fareanor3/C_courses/blob/5e58730c84283c11864b52350b6233b3947dafa7/compilation%20diagram.png)

#### La portée d'une fonction

> Une variable déclarée dans une fonction est supprimée à la fin de la fonction, elle n'est accessible que dans cette fonction.

> Une variable déclarée dans une fonction avec le mot-clé ```static``` devant n'est pas supprimée à la fin de la fonction, elle conserve sa valeur au fur et à mesure de l'exécution du programme.

> Une variable déclarée en dehors des fonctions est une variable globale, accessible depuis toutes les fonctions de tous les fichiers source du projet.

> Une variable globale avec le mot-clé ```static``` devant est globale uniquement dans le fichier dans lequel elle se trouve, elle n'est pas accessible depuis les fonctions des autres fichiers.

> Une fonction est par défaut accessible depuis tous les fichiers du projet, on peut donc l'appeler depuis n'importe quel autre fichier.

> Si on veut qu'une fonction ne soit accessible que dans le fichier dans lequel elle se trouve, il faut rajouter le mot-clé ```static``` devant.

```C
static int resultat = 0;
static int triple(int nombre)
{
    // Instructions
}
```
#### ❗ Attention mettre à jour le prototype
```H
static int triple(int nombre);
```

#### Les pointeurs

```C
printf("L'adresse de la variable age est : %p", &age); // &age: désigne l'adresse de la variable. et %p designe l'adresse
```

> variable de type pointeur, rajouter ```*```devant le nom de la variable.
```C
int *monPointeur = NULL;
```
> Dans le code :
```c
int age = 10;
int *pointeurSurAge = &age;
```

#### Envoyer un pointeur à une fonction

```C
void triplePointeur(int *pointeurSurNombre);

int main(int argc, char *argv[])
{
    int nombre = 5;

    triplePointeur(&nombre); // On envoie l'adresse de nombre à la fonction
    printf("%d", nombre); // On affiche la variable nombre. La fonction a directement modifié la valeur de la variable car elle connaissait son adresse

    return 0;
}

void triplePointeur(int *pointeurSurNombre)
{
    *pointeurSurNombre *= 3; // On multiplie par 3 la valeur de nombre
}
```
> Output:
```
15
```

> Si on place un symbole ```&``` devant un nom de variable, on obtient son adresse au lieu de sa valeur (ex. :&age).

> Si on place un symbole ```*``` devant un nom de pointeur, on obtient la valeur de la variable stockée à l'adresse indiquée par le pointeur.

> Les pointeurs constituent une notion essentielle du langage C, mais néanmoins un peu complexe au début. Il faut prendre le temps de bien comprendre comment ils fonctionnent car beaucoup d'autres notions sont basées dessus.

#### Tableau
```c
int tableau[4] = {0}; // Toutes les cases du tableau seront initialisées à 0
```

#### ❗ Attention chose a ne surtout pas faire pour aider le compilateur :
```c
int taille = 5;
int tableau[taille];
```

> boucle d'affichage des valeurs

```C
for (i = 0 ; i < 4 ; i++)
{
  printf("%d\n", tableau[i]);
}
```

#### Les chaînes de caractères

> Le type ```char``` est en fait prévu pour stocker UNE lettre

> La fonction ```printf``` peut aussi afficher un caractère. Pour cela, on doit utiliser le symbole ```%c``` (c comme caractère) : 

> On utilise donc les apostrophes pour obtenir la valeur d'une lettre.

Exemple de code de saisie claivier: 
```C
int main(int argc, char *argv[])
{
    char lettre = 0;

    scanf("%c", &lettre);
    printf("%c\n", lettre);

    return 0;
}
```

![chaine_de_characère](https://github.com/fareanor3/C_courses/blob/5e58730c84283c11864b52350b6233b3947dafa7/representation%20de%20la%20chaine%20de%20caract%C3%A8re%20salut%20en%20memoire.png)

Pour initialiser une chaîne
```C
int main(int argc, char *argv[])
{
    char chaine[] = "Salut"; // La taille du tableau chaine est automatiquement calculée

    printf("%s", chaine);

    return 0;
}
```
❗ Attention
> Ca ne marche que pour l'initialisation ! Vous ne pouvez pas écrire plus loin dans le code :
```C
chaine = "Salut";
```
#### Récupération d'une chaîne via un ```scanf```
```c
int main(int argc, char *argv[])
{
    char prenom[100];

    printf("Comment t'appelles-tu petit Zero ? ");
    scanf("%s", prenom);
    printf("Salut %s, je suis heureux de te rencontrer !", prenom);

    return 0;
}
```
#### Fonctions de manipulation des chaînes

```c
#include <string.h>`
```
```strlen``` : calculer la longueur d'une chaîne (sans compter le caractère ```\0```)
```c
size_t strlen(const char* chaine); // size_t un type spécial qui signifie que la fonction renvoie un nombre correspondant à une taille. 
```
```c
int main(int argc, char *argv[])
{
    char chaine[] = "Salut";
    int longueurChaine = 0;

    // On récupère la longueur de la chaîne dans longueurChaine
    longueurChaine = strlen(chaine);

    // On affiche la longueur de la chaîne
    printf("La chaine %s fait %d caracteres de long", chaine, longueurChaine);

    return 0;
}
````
```strcpy``` (comme « string copy ») permet de copier une chaîne à l'intérieur d'une autre.
> son prototype est :
```h
char* strcpy(char* copieDeLaChaine, const char* chaineACopier);
```
exemple:
```C
int main(int argc, char *argv[])
{
    /* On crée une chaîne "chaine" qui contient un peu de texte
    et une copie (vide) de taille 100 pour être sûr d'avoir la place
    pour la copie */
    
    char chaine[] = "Texte", copie[100] = {0};// on met 100 pour avoir de la place

    strcpy(copie, chaine); // On copie "chaine" dans "copie"

    // Si tout s'est bien passé, la copie devrait être identique à chaine
    printf("chaine vaut : %s\n", chaine);
    printf("copie vaut : %s\n", copie);

    return 0;
}
```

```strcat``` ajoute une chaîne à la suite d'une autre :
> son prototype est :
```h
char* strcat(char* chaine1, const char* chaine2);
```
exemple:
```C
int main(int argc, char *argv[])
{
    /* On crée 2 chaînes. chaine1 doit être assez grande pour accueillir
    le contenu de chaine2 en plus, sinon risque de plantage */
    char chaine1[100] = "Salut ", chaine2[] = "Mateo21";

    strcat(chaine1, chaine2); // On concatène chaine2 dans chaine1. Attention à la taille de la chaine qui ressoit !

    // Si tout s'est bien passé, chaine1 vaut "Salut Mateo21"
    printf("chaine1 vaut : %s\n", chaine1);
    // chaine2 n'a pas changé :
    printf("chaine2 vaut toujours : %s\n", chaine2);

    return 0;
}
```

