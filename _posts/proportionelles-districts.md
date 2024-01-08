---
title: 'La proportionelle en districts'
date: 2023-11-30
permalink: /posts/2023/11/blog-post-3/
tags:
  - Vulgarisation
  - Démocratie
  - Contraintes
  - Parlement
---
Dans le dernier article, on a fait un tour des principaux modes de scrutin à la proportionelle dont certains sont utilisés pour les élections parlementaires. Le problème relevé en général pour ces modes de scrutin est le manque de représentation locale (par région ou district), pour remédier à cela, certains pays font donc des scrutins à la proportionelle dans chaque disctrict. On a expliqué dans [le premier article](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/) pourquoi cela était limité. On va voir ici des méthodes plus adaptées à ce contexte appelées méthodes à la double proportionelle.

Les élections du Bundestag en Allemagne
====

En Allemagne, les votes se font au niveau des ditricts avec un double bulletin, les votant·e·s doivent désigner un·e candidat·e et un parti. Dans chaque district, on détermine l·a·e gagnant·e du scrutin majoritaire à un tour. On utilise ensuite la [méthode de Sainte Lägue](https://matthieuhervouin.github.io/posts/2012/08/blog-post-2/) en excluant les partis ayant reçu moins de 5% des voix et ayant moins de trois vainqueurs locaux. On obtient une répartition des sièges par parti, sachant qu'il y a deux fois plus de sièges que de districts. Une fois les sièges attribués aux partis, les vainqueurs locaux prennent les sièges en priorité au sein de chaque parti.

### Exemple de la méthode Allemande pour 6 sièges
Pour cet exemple, on suppose qu'on avait pas de quota pour simplifier.

| Parti         | A       | B     | C   |
| district 1    | 9       | 10    | 3   |
| district 2    | 7       | 10    | 5   |
| district 3    | 5       | 8     | 9   |
|:--------      |:-------:|------:| ---:|
| total         | 21      | 29    | 17  |
|:--------      |:-------:|------:| ---:|
| division par 1| 20      | 29    | 17  |
| division par 3| 6.7     | 9.7   | 5.7 |
| division par 5| 4.2     | 5.8   | 3.2 | 
|=======================================|
| nb de sièges  | 2       | 3     | 1   |
 
Dans cet exemple, le parti B obtient 3 sièges dont deux sont assignés aux vainqueurs des districts 1 et 2, le parti A obtient 2 sièges et le parti C un qui est attribué au vainqueur du district 3.

Effets sur la proportionalité locale et globale
-----
La méthode de Sainte Lägue, a tendance à favoriser les partis de petite taille comme on a pu le voir dans l'article précédent, on limite cependant l'accès pour les petits partis avec les quotas. Le fait de sélectionner des vainqueurs locaux n'a pas d'effet sur la proportionalité à l'échelle nationale, la question est : à quel point les localités sont-elles représentées ? Dans le pire des cas, chaque vainqueur local est isolé et ne peut donc pas obtenir de siège au parlement par le scrutin proportionnel. 

### Exemple d'un cas extrème pour 12 sièges
Pour cet exemple, on suppose qu'on avait pas de quota pour simplifier.

| Parti         | A       | B     | C   |  D  |  E   |
| district 1    | 8       | 8     | 8   |  9  |  0   |
| district 2    | 8       | 8     | 8   |  0  |  9   |
| district 3    | 10      | 12    | 11  |  0  |  0   |
| district 4    | 8       | 15    | 10  |  0  |  0   |
| district 5    | 12      | 10    | 11  |  0  |  0   |
| district 6    | 11      | 9     | 13  |  0  |  0   |
|:--------      |:-------:|------:| ---:|----:| ----:|
| total         |  57     | 62    | 61  |  9  |  9   |
|:--------      |:-------:|------:| ---:|----:| ----:|
| division par 1| 57      | 62    | 61  | 0   |  0   |
| division par 3| 19      | 20.7  | 20.3| 0   |  0   |
| division par 5| 11.4    | 12.4  | 12.2| 0   |  0   |
| division par 7| 8.1     | 8.9   | 8.7 | 0   |  0   |
| division par 9| 6.3     | 6.9   | 6.8 | 0   |  0   |
|====================================================|
| nb de sièges  | 3       | 3     | 3   | 0   |  0   |

Ici les partis C et D n'obtiennent aucun sièges car ils représentent seulement 9&frasl;198 = 4.5 % des votant·e·s chacun et sont donc éliminés. Pourtant si on ne les avait pas éliminés au début du processus, ils auraient obtenu 1 siège chacun avec le scrutin de Sainte Lägue, ils ont de plus gagné leurs éléctions au niveau local.

Pour résumer, le système allemand est centré sur la proportionelle au niveau global, il va ensuite attribuer les sièges à l'intérieur des partis de manière à ce que le plus possible de districts aient un·e représentant·e local·e qui corresponde au vote des majorités locales. C'est la priorité inverse de celle qui était donnée en France sous la IVème république.






Sources
=====
[Elections allemandes](https://fr.wikipedia.org/wiki/Élections_fédérales_allemandes_de_2021#Organisation)
