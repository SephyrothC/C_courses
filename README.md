![banner](https://raw.githubusercontent.com/fareanor3/C_courses/main/banner.jpg?token=AOSHXRWF3YD6RADHQ6HIPY3BDAR7U)
# C_courses

##  Mind the openclassroom courses

___

>card on the C language from the Open Classroom course ( https://openclassrooms.com/fr/courses/19980-apprenez-a-programmer-en-c/13300-vous-avez-dit-programmer ). 

___

####  code minimaliste :
```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
  printf("Bonjour");
  return 0;
}

|'But'|*Fonction*|
| :--------: |:-----:|
| `affichage`  |   printf("Bonjour")  |
|`entée utilisateur`|scanf("%d", &age)|
|`retour à la ligne (= « Entrée »)` | \n |
|`tabulation`|\t|
|`commentaire`|//|
|`debut & fin commentaire`|/* & *\|
```

#### variable :

|'Nom du type'|*Min*|*Max*|
| :--------: |:-----:|:-----:|
|'signed char'|-127|127|
|'int'|-32 767|32767|
|'long'|-2 147 483 647|2 147 483 647|
|'float'|-1 x1037|1 x1037|
|'double'|-1 x1037|1 x1037|

> Généralement on utilise pour un nombre entier : ```int``` et pour un flottant un ```double```

#### ❗ Attention : 
> Les trois premiers types (signed char,int,long) permettent de stocker des nombres entiers :
Les deux derniers (float,double) permettent de stocker des nombres décimaux (appelés nombres flottants) : 13.8, 16.911…

> ```unsigned``` est un mot clée permetant de stoquer que des nombre possitif 
const pour déclarer une constante

#### Afficher le contenu d'une variable :

``` printf("il vous reste %d vies rt vous etes au niveau", nombre_de_vies, niveau);```

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

``` c
nombre += 4;
nombre -= 3;
nombre *= 5;
nombre /= 3;
nombre %= 3;
```

#### La bibliothèque mathématique

``` c
#include <maths.h>
```

#### ❗ Attention tous est en bouble

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

#### if : 

```c
if (/* Votre condition */)
{
  // Instructions à exécuter si la condition est vraie
}
```

#### else :

```c
if (age >= 18) // Si l'âge est supérieur ou égal à 18
{
  printf ("Vous etes majeur !");
}
else // Sinon...
{
  printf ("Ah c'est bete, vous etes mineur !");
}```

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
}```

#### plusieur condition a la fois

|*Signification*|'Symbole'|
| :--------: |:-----:|
|`ET`|`&&`|
|`OU`|`||`|
|`NON`|`!`|

#### ex :

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