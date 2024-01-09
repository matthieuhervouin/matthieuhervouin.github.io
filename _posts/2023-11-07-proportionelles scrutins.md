---
title: 'Les modes de scrutin à la proportionelle'
date: 2023-11-06
permalink: /posts/2012/08/blog-post-2/
tags:
  - Vulgarisation
  - Démocratie
  - Contraintes
  - Parlement
---
Dans [l'article précédent](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/), on a parlé des élections parlementaires avec un scrutin à la proportionelle. Ici, on va faire le tour des principales méthodes qui existent et des propriétés bonnes ou mauvaises qu'elles peuvent avoir.

Les méthodes "classiques" de vote à la proportionelle
=====

Les mode de scrutin à la proportionelle partent tous de la même base, le nombre de siège de chaque parti doit être proportionnel au nombre de votes reçu. On ne peut malheureusement pas avoir de proportionelle réelle puisque le nombre de siège donné aux partis doit être entier, il y a donc plusieurs modes de scrutin qui diffèrent par leur manière d'allouer les sièges "non entiers". On appelle la proportionelle pure la méthode qui donnerait à chaque parti un nombre exactement proportionnel aux votes reçus, elle n'est bien sûr pas appliquée car elle donne des portions de siège, ce qui est impossible dans le cas réel.


Les méthodes à plus forte moyenne ou méthodes des diviseurs
-----

Le mode de scrutin pour les élections parlementaires de la IVème république que nous avons présenté dans l'article précédent fait partie d'une famille, celle des méthodes des diviseurs. Plus exactement elle est équivalente à la méthode des diviseurs suivante, ce que nous allons bien sûr démontrer rapidement. La méthode D'Hont consiste à diviser le nombre de vote reçus par chaque parti par une suite de diviseurs de 1 jusqu'à _m_ la taille du parlement à élire. On obtient alors un tableau de nombres décimaux dont on va simplement sélectionner les _m_ plus grands. Chaque suite croissante de _m_ entiers ou diviseurs correspond à une méthode de diviseurs donnée. On va voir d'autres méthodes possibles plus tard.

### Exemple de la méthode D'Hont pour 8 sièges

| Parti         | A       | B     | C   |
|:--------      |:-------:|------:| ---:|
| nb de votes   | 13      | 19    | 8   |
|:--------      |:-------:|------:| ---:|
| division par 1| 13      | 19    | 8   |
| division par 2| 6.5     | 9.5   | 4   |
| division par 3| 4.25    | 6.3   | 2.7 |
| division par 4| 3.25    | 4.5   | 2   | 
| division par 5| 2.6     | 3.2   | 1.6 |  
|=======================================|
| nb de sièges  | 3       | 4     | 1   |

Ici, les 8 plus grands nombres dans le tableau sont 19, 13, 9.5, 8, 6.5, 6.3 et 4.5. On alloue un siège au parti qui correspond à chacun de ces nombres et on obtient notre répartition des sièges. En général, comme dans ce cas, on a pas besoin d'écrire le tableau en entier (ici on s'est arrété à 5 et non 8). 

### Preuve: Jefferson équivault à D'Hont (pas obligatoire à lire )

Notons $n$ le nombre de votant·e·s au total, $m$ le nombre de parti et pour chaque parti $i$ de 1 à $m$, on note $n_i$ le nombre de votes reçus par $i$. On veut déjà vérifier que chaque parti $i$ obtient bien au moins  $s_j= \lfloor n_i \times \frac{n}{m} \rfloor$ où $\lfloor x \rfloor$ est l'arrondi à l'entier inférieur de $x$. (Rappel: la méthode de Jefferson commence par attribuer les sièges entiers après avoir fait le produit en croix pour reporter proportionellement le nombre de votes par parti)[voir méthode de Jefferson](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/).

Supposons qu'il existe un parti $i$ ayant obtenu moins de $s_i$ sièges, dans ce cas il doit y avoir un parti $j$ qui en a obtenu plus que $s_j$ d'où $\frac{n_j}{s_j +1} \geq \frac{n_i}{s_i}$(1).

On sait que $s_{j+1} = \lfloor \frac{m}{n} \times n_j \rfloor +1 > \frac{m}{n}\times n_j$, et $s_i = \lfloor  \frac{m}{n}\times n_i \rfloor \leq \frac{m}{n}\times n_i$. Ainsi, (1) implique $\frac{n_j}{\frac{m}{n}\times n_j}> \frac{n_j}{s_j +1} \geq \frac{n_i}{s_i} \geq \frac{n_i}{frac{m}{n}\times n_i}$ d'où $\frac{n}{m} >\frac{n}{m}$ ce qui est impossible.

On a montré que la méthode de D'Hont respecte bien les sièges alloués lors de la première étape de la méthode de Jefferson, on peut remarquer que la deuxième étape de Jefferson correspond bien à sélectionner les plus grands quotients restants (il s'agit simplement de les sélectionner un par un au lieu d'écrire le tableau).




Les méthodes au plus fort reste
-----

Les méthodes au plus fort reste ont la même base : on commence par calculer le quotient électoral. Il existe plusieurs variantes de méthodes à plus fort reste, dont la différence figure dans le calcul du quotient électoral, on va ici se concentrer sur la méthode de Hare. Le quotient de Hare est le nombre de votes $n$ divisé par le nombre de sièges du parlement $k$ (donc $\frac{n}{k}$). Pour chaque parti, on fait une division entière du nombre de vote de soutien au parti par le quotient électoral, on obtient un nouveau quotient par parti et un reste. On affecte un nombre de sièges à chaque parti correspondant à leurs quotients respectifs (on ne dépasse pas la taille du parlement car au total c'est au plus $k \times \frac{n}{n}=k$ sièges attribués). La deuxième étape est d'attribuer les sièges restants aux partis par ordre décroissant des restes. 


### Exemple de la méthode de Hare avec 8 sièges

On prend 40 votant·e·s, donc le quotient de Hare est de $\frac{40}{5}=8$.

| Parti           | A       | B     | C   |
|:--------        |:-------:|------:| ---:|
| nb de votes     | 13      | 19    | 8   |
|:--------        |:-------:|------:| ---:|
|quotient par 5   | 2       | 3     | 1   |
| reste par 5     | 3       | 4     | 3   |
|=========================================|
| nb de sièges    | 2       | 4     | 2   |

Ici, les trois partis sont ex-aequo sur le dernier siège, dans ce cas la constitution prévoit un moyen simple de départager (en France c'est l'âge des candidat·e·s) ici on suppose que c'est l'ordre le parti C gagne le dernier siège par départage. On a obtenu un résultat différent de celui calculé par la méthode de D'Hont, ce n'est pas une exception, ces deux méthodes ont des objectifs assez différents sur la répartition des sièges restants après l'attribution des sièges "entiers".

NB: A noter qu'ici on compare les reste des divisions euclidiennes par le quotient, mais on pourrait tout aussi bien comparer les restes décimaux. En effet quand on fait la division entière de $a$ par $b$, on cherche le quotient $q$ et le reste $q$. On a alors  $r = a - b \times q$ et le reste décimal est $\frac{a}{q}-b =\frac{r}{q}$. Les restes de division euclidiennes et restes décimaux sont donc proportionnels, donc prendre les plus grands restes entiers ou décimaux revient au même. Dans les applications des méthodes de plus fort reste, on trouve ainsi les deux possibilités de comptage.


Différences entre méthodes de diviseurs et méthodes à plus fort reste
-----

L'esprit de la méthode de D'Hont est de maximiser le nombre minimal de vote par siège pour un parti, donc de minimiser la surreprésentation des parti.

### Représentation des partis

On prend 40 votant·e·s pour 8 sièges, donc le quotient de Hare est de $\frac{40}{8}=5$. On va calculer les quotients éléctoraux des partis, c'est à dire le nombre de sièges obtenu par votant·e·s.

| Parti           | A       | B     | C   |
|:--------        |:-------:|------:| ---:|
| nb de votes     | 12      | 20    | 8   |
|:--------        |:-------:|------:| ---:|
| sièges D'Hont   | 3       | 4     | 1   |
| sièges Hare     | 2       | 4     | 2   |
|=========================================|
| quotient D'Hont | 1/4     | 1/5   | 1/8 |
| quotient Hare   | 1/6     | 1/5   | 1/2 |

On peut voir que le plus grand quotient est de 1/4 pour la méthode de D'Hont et 1/2 pour Hare. Le parti C est surreprésenté par rapport aux autres partis avec la métode de Hare, celle de D'Hont a pour but de limiter cette surreprésentation.

Le paradoxe de l'Alabama
-----

Le paradoxe d'Alabama tient son nom d'un cas d'application d'une méthode du plus fort reste aux Etats-Unis. La chambre des représentant·e·s devait sélectionner un nombre de représentant·e·s par état proportionnel à sa population, et C.W. Seaton qui travaillait au bureau du recensement a remarqué un défaut étonnant. Si le nombre total de représentant·e·s passait de 299 à 300, l'état d'Alabama passait de 8 à 7 représentant·e·s, un paradoxe étonnant qui est propre aux méthodes à plus fort reste.

### Exemple

Pour cet exemple on prend 10 000 votant·e·s avec 4 partis et on regarde les répartitions données par la méthode de Hare pour une taille de parelement $k$ égale à 5 ou 6.

| Parti           | A       | B     | C    | D   |
|:--------        |:-------:|------:| ----:| ---:|
| nb de votes     | 5670    | 3850  | 420  | 60  |
|:--------        |:-------:|------:| ----:|----:|
| quotient k=5    | 183     | 124   | 13   | 1   |
| reste k=5       | 0.141   | 0.355 | 0.566|0.938|
| sièges k=5      | 183     | 124   | 14   | 2   |
|================================================|
| quotient k=6    | 183     | 124   | 13   | 1   |
| reste k=6       | 0.708   | 0.740 | 0.608|0.944|
| sièges k=6      | 184     | 125   | 14   | 1   |

Ici, on peut voir qu'après avoir augmenté la taille du parlement de 1, le parti C a perdu un siège, ce qui est un point faible de la méthode de Hare. Ce paradoxe arrive très rarement mais est déjà apparu en situation réelle, il compromet don la méthode de Hare qui semble être moins intéressante que celle de D'Hont pour laquelle ce paradoxe est impossible.

Effets du mode de scrutin sur la représentation
=====

Avec les deux sections précédentes, on peut penser que la méthode de Hare est définitivement à éliminer, puisqu'elle tend à surreprésenter les partis plus que celle de D'Hont, et on peut se retrouver face au paradoxe de l'Alabama. Il y a aussi une autre différence qui tend plus pour celle de Hare cette fois, elle tend à favoriser les plus petits partis tandis que celle de D'Hont favorise les plus grands. Ainsi sur l'exemple à40 votant·e·s, il restait un siège à départager, la méthode de D'Hont l'a alloué au parti A (le deuxième plus gros) et celle de Hare l'a alloué au parti C qui lui est plus petit.


Favoriser les grands ou petits partis
-----

Décider entre favoriser les plus grands ou plus petits partis est une question assez complexe, en favorisant les plus grands, on va avoir une proportionnalité plus forte, mais favoriser les plus petits est important pour le multipartisme. Il existe plusieurs indices pour mesurer la disproportionalité d'une élection, il y a deux familles comme pour les modes de scrutin : la première se base sur la division du nombre de sièges obtenus par le nombre de votant·e·s et la deuxième sur les différences entre le pourcentage de votant·e·s et le pourcentage de sièges obtenus. Décider de favoriser les petits ou grands partis est une question politique, en France on a privilégié des systèmes avec effet de "barrage", et on privilégie principalement les gros partis, mais d'autres pays en Europe ont des sytèmes qui privilégient les plus petits partis.


La méthode des divieurs impairs
-----

Dans les méthodes des diviseurs, choisir la suite de diviseurs est très important, la méthode de D'Hont favorise principalement les grands partis, mais en prenant une suite qui croit plus vite, on peut changer cela. (Rappel : pour la méthode de D'Hont la suite des diviseurs sont les entiers de 1 à la taille du parlement). La méthode de Sainte-Laguë utilise elle les entiers impairs, ainsi si le premier siège est plus facile à obtenir pour un parti, les suivants seront plus durs. L'idée est de favoriser la diversité de représentation plutôt que la proportionelle stricte.

### Exemple de la méthode Sainte-Laguë pour 8 sièges

| Parti         | A       | B     | C   |
|:--------      |:-------:|------:| ---:|
| nb de votes   | 13      | 19    | 8   |
|:--------      |:-------:|------:| ---:|
| division par 1| 13      | 19    | 8   |
| division par 3| 4.3     | 6.3   | 2.7 |
| division par 5| 2.6     | 3.8   | 1.6 |
| division par 7| 1.9     | 2.7   | 1.1 | 
| division par 9| 1.4     | 2.1   | 0.9 |  
|=======================================|
| nb de sièges  | 2       | 4     | 2   |


Ici, les 8 plus grands chiffres obtenus dans le tableau sont 19, 13, 9, 6.3, 4.3, 3.8, et 2.7 deux fois. On obtient donc le même résultat qu'avec la méthode de Hare, ce qui ne sera pas toujours le cas. Avec cette méthode, le premier siège est de très loin le plus facile à obtenir, elle tend donc à faire apparaître beaucoup de très petits partis, lorsqu'elle était appliquée (dans les pays scandinaves principalement) elle tendait à rendre le parlement instable pour les questions de majorité. Le choix a donc été fait dans ces pays d'adapter ce mode de scrutin en modifiant le premier diviseur à 1.4, il devient donc plus difficile d'obtenir le premier siège, ce qui évite d'avoir une multitude de partis à 1 siège. Cette variante de la méthode de Sainte-Laguë va donc favoriser les partis de moyenne taille (qui auraient au moins un siège à la proportionelle pure).
 


Proportionelle vs représentation locale
=====

Un des reproches fait aux élections à la proportionelle est que les régions sont souvent mal représentées, au niveau national chaque parti obtient ses sièges mais les partis régionaux ont souvent du mal à se faire une place. Pour favoriser une représentation locale, certains pays optent pour des scrutins à la proportionelle indépendants dans chaque région, c'était le cas de la France sous la IVème république. Dans [l'article précédent](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/) on a vu que cette stratégie ne permet pas d'avoir une répartition proportionelle des sièges à l'échelle nationale, il y a un conflit entre la proportionelle locale et nationale. La prochaine fois, on verra des modes de scrutins adaptés à cette problématique, notamment un qui est en place en Allemagne.



Sources
=====
[scrutin proportionnel (wiki)](https://fr.wikipedia.org/wiki/Scrutin_proportionnel_plurinominal)
[Scrutins et proportionnalité](https://fr.wikipedia.org/wiki/Systèmes_électoraux_et_proportionnalité#Méthodes_par_diviseurs)
[Paradoxe d'Alabama](https://fr.wikipedia.org/wiki/Paradoxe_de_l%27Alabama)
