---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Unités

Toute la physique s'exprime aujourd'hui de manière quantitative au moyen d'équations, de constantes...  Pour pouvoir exprimer de manière "universelle" les données obtenues dans le développement d'un cadre théorique ou lors d'une expérience, il est important de définir un système d'unités cohérent et exhaustif permettant de donner une mesure à toute grandeur physique sans  contradiction entre les différentes définitions.

## Unités fondamentales


Un certain nombre d'unités «de base» ou «fondamentales» doivent être définies à partir:

* soit d'un rapport à des constantes fondamentales ou des phénomènes physiques bien particuliers que décrivent très bien certains cadres théoriques
* soit au moyen d'un objet-étalon définissant la valeur 1 d'une unité données.

Les unités qu'on définit ainsi sont appelées les unités fondamentales. On peut alors définir un certain nombre d'unités secondaires qui ne font que dériver des unités fondamentales: on ne les obtient pas directement lors d'une expérience.

Les unités fondamentales (et les autres) sont définies lors de Conférences Générales des Poids et Mesures (CGPM).


````{important} __Fondamental : Les 7 unités fondamentales__

* Unité de temps: la seconde (s)
* Unité de longueur: le mètre (m)
* Unité de masse: le kilogramme (kg)
* Unité de courant électrique: l'Ampère (A)
* Unité de température thermodynamique: le Kelvin (K)
* Unité de quantité de matière: la mole (mol)
* Unité d'intensité lumineuse: le candela (cd)
````

````{dropdown} Remarque
Ces unités sont définies à partir:
* soit d'un rapport à des constantes fondamentales ou des phénomènes physiques bien particuliers que décrivent très bien certains cadres théoriques
* soit au moyen d'un objet-étalon définissant la valeur 1 d'une unité données.
````

## Unités dérivées - Présentation


Le système d'unités internationales est le système d'unité retenus par la Conférence Générale des Poids et Mesures pour quantifier toutes les grandeurs physiques mesurables. Il compte 7 unités fondamentales (citées précédemment) auxquelles s'ajoutent un certain nombre d'unités dérivées permettant de clarifier le écritures.


````{admonition} Exemples d'unités fondamentales
:class: note
| Grandeur | Unités | Symbole |
| :- | :-: | -: |
| Fréquence | Hertz | Hz |
| Force | Newton | N |
| Pression | Pascal | Pa |
| Potentiel électrique | Volt | V |
| Energie | Joule | J |

````

````{dropdown} Remarque
D'autres unités, qui ne font pas partie du système d'unités internationales existent pour décrire les mêmes grandeurs. Exemple : la pression s'exprime aussi en bar ou en mmHg.

Certaines puissances ou produits d'unités fondamentales décrivent des grandeurs physiques particulières. La vitesse s'exprime en $m.s^{-1}$ ou le volume en $m^3$
````

## Méthode : Expression des unités dérivées.

````{admonition} Exercice 
:class: attention
Exprimer l'unité Newton (N) en fonction des unités fondamentales
````

_Pour répondre à cette question, il faut utiliser des relations physiques connues reliant une grandeur dont l'unité est celle étudiée aux unités fondamentales._

````{dropdown} Correction
> Le Newton est l'unité utilisé pour l'intensité des forces. Le principe fondamental de la dynamique s'écrit:
>
>$$\frac{d \overrightarrow{p}}{dt} = \overrightarrow{F}$$
>
> avec $\overrightarrow{p} = m\overrightarrow{v}$ la quantité de mouvement dont l'unité est donc des $kg.m.s^{-1}$.
>
>La dérivée par rapport au temps revient, d'un point dimensionnelle à diviser par le temps. Il vient comme unité $kg.m.s^{-2}$
````

````{dropdown} A retenir
On retiendra que la dérivée par rapport au temps revient, d'un point dimensionnelle à diviser par le temps. Plus généralement, dériver par rapport à une grandeur X d'unité U revient à diviser l'unité par U.
````

````{admonition} Exercice 
:class: attention
Exprimer l'unité Joule (J) en fonction des unités fondamentales
````

````{dropdown} Correction
On peut utiliser l'expression de l'énergie cinétique $E_c = \frac{1}{2} m v^2$ il vient comme unité $kg.m^2.s^{-2}$
````

````{admonition} Exercice 
:class: attention
Exprimer l'unité Coulomb (C) en fonction des unités fondamentales
````

````{dropdown} Correction
Le Coulomb est l'unité de charge électrique. L'intensité électrique est définie comme la quantité de charge passant une surface par unité de temps, donc le Coulomb s'exprime comme $A.s^{-1}$
````

# Homogénéité et analyse dimensionnelle

Une relation est homogène si tous les termes sommés ont la même unité.  
Tester l'homogénéité d'une relation est extrêmement importante. Cela permet:

* De déterminer la forme d'une grandeur physique quand on connaît ses dépendances.
* De déterminer si le résultat d'un calcul est possible ou non: tester l’homogénéité d'une expression est une manière simple de vérifier si son calcul est bon.

## Homogénéité des relations physiques

__UN RÉSULTAT NON HOMOGÈNE EST UNE ERREUR GRAVE EN PHYSIQUE.__

_Pour vérifier l'homogénéité d'une expression, il n'est pas nécessaire (__et même déconseillé__) de revenir aux unités fondamentales. Le but d'une telle vérification est de pouvoir déterminer __rapidement__ si un résultat n'est pas complètement faux._


### Méthode : Vérification rapide de l'homogénéité des expressions.

````{admonition} Exercice 
:class: attention
Quelles sont parmi les expressions ci-dessous, celles qui sont homogènes ? Vous ne devez pas passer plus de deux minutes (plus tard, ce temps sera plus court) pour chaque expression :

* $UI^2 = RI^2\tau$
* $\frac{1}{2} m v^2 = mgz$
````

````{dropdown} Correction
> * Première relation : Nous sommes en électrocinétique. On peut remarquer que $UI$ est une puissance, tout comme $RI^2$. Il reste une intensité à gauche et un temps à droite : ce n'est pas homogène.
> 
> * Deuxième équation : On reconnaître des expressions venues de la mécanique. Il s'agit d'une égalisation de deux énergies (cinétique à gauche et potentielle à droite).
````

## Analyse dimensionnelle

### Principe général de l'analyse dimensionnelle
````{important} __Fondamental : __
Les unités fondamentales sont __indépendantes__ et ne peuvent donc pas s'exprimer les unes en fonction des autres. Cela signifie que si l'on exprime chaque expressions d'une formules en fonction des unités fondamentales, __les puissances de celles-ci doivent être égales.__ Cette propriété permet de déterminer une formule possible pour certaines problèmes.
````

```{dropdown} Remarque
Comme on va le voir, une analyse dimensionnelle permet de connaître une formule à un facteur près car on peut toujours respecter l'homogénéité d'une expression en multipliant celle-ci par une constante sans dimension.
```

### Méthode : Analyse dimensionnelle

````{admonition} Exercice 
:class: attention
Un électron de charge $e$ qui subit une accelération $a$ perd une puissance (on parle de freinage par rayonnement) $P$. L'étude de ce phénomène est relativiste et l'on sait que l'expression de $P$ fait intervenir la célérité de la lumière dans le vide $c$ et la perméabilité du vide $\epsilon_0$ dont l'unité est $s^4.A^{2}.kg^{-1}.m^{-3}$ sous forme de produit. On peut donc écrire $P$ sous la forme :

$P = k e^{\alpha} c^{\beta} \epsilon_0^{\gamma} a^{\zeta}$ avec k une constante sans dimension.

Déterminer les exposants $\alpha, \beta, \gamma$ et $\zeta$.
````

````{dropdown} Correction
>Comme on l'a dit, on ne peut exprimer une unité fondamentale en fonction d'une autre. Chaque grandeur d'une égalité doit donc avoir la même unité exprimer au moyen des unités fondamentales. Commençons par exprimer les unités de $P$ et $k e^{\alpha} c^{\beta} \epsilon_0^{\gamma} a^{\zeta}$.
>
>Le premier a pour unité $kg.m^2.s^{-3}$
>
>Le second a pour unité (on rappelle que le Coulomb s'exprime comme des $A.s$) ${(A.s)}^{\alpha}.{(m.s^{-1})}^{\beta}.{(s^4.A^{2}.kg^{-1}.m^{-3})}^{\gamma}.{(m.s^{-2})}^{\zeta}$ soi en réorganisant $A^{\alpha - 2 \gamma}.s^{\alpha - \beta - 2 \zeta}.m^{\beta + 3 \gamma + \zeta}.kg^{\gamma}$. En identifiant les puissances, il vient :
>
>$$
\begin{cases}
\alpha + 2 \gamma &= 0\\
\alpha - \beta + 4 \gamma - 2 \zeta&= -3\\
\beta - 3 \gamma + \zeta &= 2\\
-\gamma &= 1\\
\end{cases}
$$
>	
>On obtient un système d'équation qu'il faut résoudre. Il vient assez facilement :
>
>$$\begin{cases}
\gamma &= -1 \\
\alpha &= 2 \\
\zeta &= 2 \\
\beta &= -3 \\
\end{cases}
$$
>
>Il vient la formule :
>
>$$P = k \frac{q^2 a^2}{\epsilon_0 c^3}$$
````