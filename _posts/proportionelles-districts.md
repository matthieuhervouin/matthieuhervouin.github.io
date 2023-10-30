---
title: 'Pour un parlement à la proportionelle, paritaire et représentatif des régions'
date: 2023-11-06
permalink: /posts/2012/08/blog-post-2/
tags:
  - Vulgarisation
  - Démocratie
  - Contraintes
  - Parlement
---
Dans [l'article précédent](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/), on a parlé des élections parlementaires avec un scrutin à la proportionelle. Ici, on va présenter d'autres scrutins similaires dont certains ont pour but de sélectionner un parlement représentatif au niveau des partis mais aussi des districts (chaque district doit avoir un nombre fixé de représentant), un dernier très récent rajoute un autre objectif, celui de respecter la contrainte de la parité hommes/femmes (il présente aussi un moyen de rajouter d'autres contraintes comme la représentation des catégories socio-professionelles par exemple).

Les méthodes "classiques" de vote à la proportionelle
=====

Les méthodes à plus forte moyenne ou méthodes des diviseurs
-----

Le mode de scrutin pour les élections parlementaires de la IVème république que nous avons présenté dans l'article précédent fait partie d'une famille, celle des méthodes des diviseurs. Plus exactement elle est équivalente à la méthode des diviseurs suivante, ce que nous allons bien sûr démontrer rapidement. La méthode D'Hont consiste à diviser le nombre de vote reçus par chaque parti par une suite de diviseurs de 1 jusqu'à _m_ la taille du parlement à élire. On obtient alors un tableau de nombres décimaux dont on va simplement sélectionner les _m_ plus grands. Chaque suite croissante de _m_ entiers ou diviseurs correspond à une méthode de diviseurs donnée. On va voir d'autres méthodes possibles plus tard.

### Exemple de la méthode D'Hont pour 5 sièges

| Parti         | A       | B     | C   |
|:--------      |:-------:|------:| ---:|
| nb de votes   | 15      | 20    | 9   |
|:--------      |:-------:|------:| ---:|
| division par 1| 15      | 20    | 9   |
| division par 2| 7.5     | 10    | 4.5 |
| division par 3| 5       | 6.7   | 3   |
|=======================================|
| nb de sièges  | 2       | 2     | 1   |

Ici, les 5 plus grands nombres dans le tableau sont 20, 15, 10, 9 et 7.5. On alloue un siège au parti qui correspond à chacun de ces nombres et on obtient notre répartition des sièges. En général, comme dans ce cas, on a pas besoin d'écrire le tableau en entier (ici on s'est arrété à 3 et non 5).

### Preuve: Jefferson équivault à D'Hont (pas obligatoire à lire )

Notons _n_ le nombre de votant·e·s au total, _m_ le nombre de parti et pour chaque parti _i_ de 1 à _m_, on note _n(i)_ le nombre de votes reçus par _i_. On veut déjà vérifier que chaque parti _i_ obtient bien au moins _s(j)=int(n(i)*m&frasl;n)_ où _int(x)_ est l'arrondi à l'entier inférieur de _x_. (Rappel: la méthode de Jefferson commence par attribuer les sièges entiers après avoir fait le produit en croix pour reporter proportionellement le nombre de votes par parti)[voir méthode de Jefferson](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/).

Supposons qu'il existe un parti _i_ ayant obtenu moins de _s(i)_ sièges, dans ce cas il doit y avoir un parti _j_ qui en a obtenu plus que _s(j)_ d'où _ n(j)&frasl;(s(j)+1) &#8925; n(i)&frasl;s(i).

Dans ce cas, on a _s(j)+1= int(s(j)*m&frasl;n) + 1 &#62 s()*m&frasl;n; &#8925;_. Ainsi, on a _n&#8925;m = n(j)/(n(j)*m&frasl;n) &#62; n(j)&frasl;s(j) &#8925 n(i)&frasl;s(j)_. Or comme par définition de int() on a _s(i) &#8924;n(i)*m&frasl;n_ donc _n(i)&frasl;s(i) &#8925; n&frasl;m_, on obtient que _n&frasl;m &#62; n&frasl;m_ ce qui est impossible.

On a montré que la méthode de D'Hont respecte bien les sièges alloués lors de la première étape de la méthode de Jefferson, on peut remarquer que la deuxième étape de Jefferson correspond bien à sélectionner les plus grands quotients restants (il s'agit simplement de les sélectionner un par un au lieu d'écrire le tableau).




Les méthodes au plus fort reste
-----


Différences entre méthodes de diviseurs et méthodes à plus fort reste
-----


La proportionelle à deux dimensions
=====

La proportionelle à trois dimensions ou plus
=====


Sources
=====

Bi proportionnel
------


Autre
-----
[scrutin proportionnel (wiki)](https://fr.wikipedia.org/wiki/Scrutin_proportionnel_plurinominal)
[Scrutins et proportionnalité](https://fr.wikipedia.org/wiki/Systèmes_électoraux_et_proportionnalité#Méthodes_par_diviseurs)

