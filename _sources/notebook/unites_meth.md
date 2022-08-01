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
# Exemples
_Les corrections sont en ligne._
## Expression des unités dérivées.

````{sidebar} A retenir
On retiendra que la dérivée par rapport au temps revient, d'un point dimensionnelle à diviser par le temps. Plus généralement, dériver par rapport à une grandeur X d'unité U revient à diviser l'unité par U.
````
````{admonition} Exercice 
:class: attention
Exprimer l'unité Newton (N) en fonction des unités fondamentales
````
_Pour répondre à cette question, il faut utiliser des relations physiques connues reliant une grandeur dont l'unité est celle étudiée aux unités fondamentales._

````{topic} Correction
> Le Newton est l'unité utilisé pour l'intensité des forces. Le principe fondamental de la dynamique s'écrit:
>
>$$\frac{d \overrightarrow{p}}{dt} = \overrightarrow{F}$$
>
> avec $\overrightarrow{p} = m\overrightarrow{v}$ la quantité de mouvement dont l'unité est donc des $kg.m.s^{-1}$.
>
>La dérivée par rapport au temps revient, d'un point dimensionnelle à diviser par le temps. Il vient comme unité $kg.m.s^{-2}$
````

````{admonition} Exercice 
:class: attention
Exprimer l'unité Joule (J) en fonction des unités fondamentales
````

````{topic} Correction
On peut utiliser l'expression de l'énergie cinétique $E_c = \frac{1}{2} m v^2$ il vient comme unité $kg.m^2.s^{-2}$
````

````{admonition} Exercice 
:class: attention
Exprimer l'unité Coulomb (C) en fonction des unités fondamentales
````

````{topic} Correction
Le Coulomb est l'unité de charge électrique. L'intensité électrique est définie comme la quantité de charge passant une surface par unité de temps, donc le Coulomb s'exprime comme $A.s^{-1}$
````

## Vérification rapide de l'homogénéité des expressions.

````{admonition} Exercice 
:class: attention
Quelles sont parmi les expressions ci-dessous, celles qui sont homogènes ? Vous ne devez pas passer plus de deux minutes (plus tard, ce temps sera plus court) pour chaque expression :

* $UI^2 = RI^2\tau$
* $\frac{1}{2} m v^2 = mgz$
````
_Une telle vérification doit être __rapide__. Elle serviara à la relecture après un calcul._

````{topic} Correction
> * Première relation : Nous sommes en électrocinétique. On peut remarquer que $UI$ est une puissance, tout comme $RI^2$. Il reste une intensité à gauche et un temps à droite : ce n'est pas homogène.
> 
> * Deuxième équation : On reconnaître des expressions venues de la mécanique. Il s'agit d'une égalisation de deux énergies (cinétique à gauche et potentielle à droite).
````

(andim_meth)=
## Analyse dimensionnelle

````{admonition} Exercice 
:class: attention
Un électron de charge $e$ qui subit une accelération $a$ perd une puissance (on parle de freinage par rayonnement) $P$. L'étude de ce phénomène est relativiste et l'on sait que l'expression de $P$ fait intervenir la célérité de la lumière dans le vide $c$ et la perméabilité du vide $\epsilon_0$ dont l'unité est $s^4.A^{2}.kg^{-1}.m^{-3}$ sous forme de produit. On peut donc écrire $P$ sous la forme :

$P = k e^{\alpha} c^{\beta} \epsilon_0^{\gamma} a^{\zeta}$ avec k une constante sans dimension.

Déterminer les exposants $\alpha, \beta, \gamma$ et $\zeta$.
````

````{topic} Correction
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

__Quelques exercices d'applications sont disponibles [en ligne](https://stanislas.edunao.com/mod/quiz/view.php?id=12808). Il est vivement conseillé de les traiter.__