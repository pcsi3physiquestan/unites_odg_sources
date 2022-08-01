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

````{topic} Introduction
Toute la physique s'exprime aujourd'hui de manière quantitative au moyen d'équations, de constantes...  Pour pouvoir exprimer de manière "universelle" les données obtenues dans le développement d'un cadre théorique ou lors d'une expérience, il est important de définir un système d'unités cohérent et exhaustif permettant de donner une mesure à toute grandeur physique sans  contradiction entre les différentes définitions.
````

## Unités fondamentales

````{sidebar} Principe
Un certain nombre d'unités «de base» ou «fondamentales» doivent être définies à partir:

* soit d'un rapport à des constantes fondamentales ou des phénomènes physiques bien particuliers que décrivent très bien certains cadres théoriques
* soit au moyen d'un objet-étalon définissant la valeur 1 d'une unité données.

Les unités qu'on définit ainsi sont appelées les unités fondamentales. On peut alors définir un certain nombre d'unités secondaires qui ne font que dériver des unités fondamentales: on ne les obtient pas directement lors d'une expérience.

Les unités fondamentales (et les autres) sont définies lors de Conférences Générales des Poids et Mesures (CGPM).
````
````{important} __Les 7 unités fondamentales__

* Unité de temps: la seconde (s)
* Unité de longueur: le mètre (m)
* Unité de masse: le kilogramme (kg)
* Unité de courant électrique: l'Ampère (A)
* Unité de température thermodynamique: le Kelvin (K)
* Unité de quantité de matière: la mole (mol)
* Unité d'intensité lumineuse: le candela (cd)
````

## Unités dérivées

````{topic} Introduction
Le système d'unités internationales (SI) est le système d'unité retenus par la Conférence Générale des Poids et Mesures pour quantifier toutes les grandeurs physiques mesurables. Il compte 7 unités fondamentales (citées précédemment) auxquelles s'ajoutent un certain nombre d'unités dérivées permettant de clarifier le écritures.
````


````{sidebar} Remarque
D'autres unités, qui ne font pas partie du système d'unités internationales existent pour décrire les mêmes grandeurs. Exemple : la pression s'exprime aussi en bar ou en mmHg.

Certaines puissances ou produits d'unités fondamentales décrivent des grandeurs physiques particulières. La vitesse s'exprime en $m.s^{-1}$ ou le volume en $m^3$
````
````{admonition} Exemples d'unités dérivées
:class: note
| Grandeur | Unités | Symbole |
| :- | :-: | -: |
| Fréquence | Hertz | Hz |
| Force | Newton | N |
| Pression | Pascal | Pa |
| Potentiel électrique | Volt | V |
| Energie | Joule | J |

````


## Homogénéité et analyse dimensionnelle

Une relation est homogène si tous les termes sommés ont la même unité.  
Tester l'homogénéité d'une relation est extrêmement importante. Cela permet:

* De déterminer la forme d'une grandeur physique quand on connaît ses dépendances.
* De déterminer si le résultat d'un calcul est possible ou non: tester l’homogénéité d'une expression est une manière simple de vérifier si son calcul est bon.

### Homogénéité des relations physiques

__UN RÉSULTAT NON HOMOGÈNE EST UNE ERREUR GRAVE EN PHYSIQUE.__

_Pour vérifier l'homogénéité d'une expression, il n'est pas nécessaire (__et même déconseillé__) de revenir aux unités fondamentales. Le but d'une telle vérification est de pouvoir déterminer __rapidement__ si un résultat n'est pas complètement faux._

## Analyse dimensionnelle

### Principe général de l'analyse dimensionnelle
```{sidebar} Remarque
Comme on va le voir, une analyse dimensionnelle permet de connaître une formule à un facteur près car on peut toujours respecter l'homogénéité d'une expression en multipliant celle-ci par une constante sans dimension.
```
````{important}
Les unités fondamentales sont __indépendantes__ et ne peuvent donc pas s'exprimer les unes en fonction des autres. Cela signifie que si l'on exprime chaque expressions d'une formules en fonction des unités fondamentales, __les puissances de celles-ci doivent être égales.__ Cette propriété permet de déterminer une formule possible pour [certains problèmes](andim_meth).
````
