---
title: 'Les élection parlementaires en Europe, proportionalité et localité'
date: 2024-01-09
permalink: /posts/2024/01/blog-post-3/
tags:
  - Vulgarisation
  - Démocratie
  - Contraintes
  - Parlement
---
Dans le dernier article, on a fait un tour des principaux modes de scrutin à la proportionelle dont certains sont utilisés pour les élections parlementaires. Le problème relevé en général pour ces modes de scrutin est le manque de représentation locale (par région ou district), pour remédier à cela, certains pays font donc des scrutins à la proportionelle dans chaque disctrict. On a expliqué dans [le premier article](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/) pourquoi cela était limité. On va voir ici des méthodes appelées proportionelles mixtes en prenant l'exemple de l'Allemagne.

Pour résumer, le système allemand est centré sur la proportionelle au niveau global, il va ensuite attribuer les sièges à l'intérieur des partis de manière à ce que le plus possible de districts aient un·e représentant·e local·e qui corresponde au vote des majorités locales. C'est la priorité inverse de celle qui était donnée en France sous la IVème république.

Les élections du Bundestag en Allemagne jusqu'en 2023
====

NB: Il y a beaucoup d'exceptions et d'ajustements prévus pour les élections du parlement allemand, par souci de clarté, j'en ai ommis plusieurs.

En Allemagne, jusqu'à l'année dernière, les votes se font au niveau des ditricts avec un double bulletin, les votant·e·s doivent désigner un·e candidat·e et un parti. Dans chaque district, on détermine l·a·e gagnant·e du scrutin majoritaire à un tour. On utilise ensuite la [méthode de Sainte Lägue](https://matthieuhervouin.github.io/posts/2012/08/blog-post-2/) en excluant les partis ayant reçu moins de 5% des voix et ayant moins de trois vainqueurs locaux. On obtient une répartition des sièges par parti, en donnant la priorité aux vainqueurs locaux. Il y a ensuite deux étapes d'ajustement, si un parti a plus de vainqueurs directs que le nombre de sièges déjà attribué, on lui ajoute les sièges correspondants, on ajoute ensuite des sièges aux autres partis pour rééquilibrer la balance et garder la proportionalité. La particularité de ce système de vote est que le nombre de député·e·s n'est pas fixe, il change d'une élection à l'autre en fonction des ajustements.


### Exemple de la méthode Allemande pour 6 sièges
Pour cet exemple, on suppose qu'on n'avait pas de quota pour simplifier.

| Parti         | A       | B     | C   |
| district 1    | 9       | 10    | 3   |
| district 2    | 7       | 11    | 4   |
| district 3    | 5       | 8     | 9   |
|:--------      |:-------:|------:| ---:|
| total         | 21      | 29    | 16  |
|:--------      |:-------:|------:| ---:|
| division par 1| 20      | 29    | 16  |
| division par 3| 6.7     | 9.7   | 5.3 |
| division par 5| 4.2     | 5.8   | 3.2 | 
|=======================================|
| nb de sièges  | 2       | 3     | 1   |
 
Dans cet exemple, le parti B obtient 3 sièges dont deux sont assignés aux vainqueurs des districts 1 et 2, le parti A obtient 2 sièges et le parti C un qui est attribué au vainqueur du district 3. Dans cet exemple, il n'y a pas d'ajustement à faire, mais cela peut arriver et arrive souvent dans des cas réels.

### Exemple d'ajustement pour 6 sièges
Pour cet exemple, on suppose qu'on avait pas de quota pour simplifier.

| Parti         | A       | B     | C   |
| district 1    | 8       | 7     | 7   |
| district 2    | 8       | 7     | 7   |
| district 3    | 8       | 7     | 7   |
| district 4    | 0       | 22    | 0   |
|:--------      |:-------:|------:| ---:|
| total         | 24      | 43    | 21  |
|:--------      |:-------:|------:| ---:|
| division par 1| 24      | 43    | 21  |
| division par 3| 8       | 14.3  | 7   |
| division par 5| 4.8     | 8.6   | 4.2 | 
|=======================================|
| nb de sièges  | 2       | 3     | 1   |

Ici, la méthode de Sainte-Lägue nous donne une répartition qui ne colle pas avec les sièges à attribuer pour les vainqueurs de scrutins majoritaires. En effet, le parti A gagne 3 scrutins locaux mais ne remporte que deux sièges sur l'élection à l'échelle nationale. On lui ajoute donc un siège pour que les majorités locales soient respectées, ce qui fait donc perdre la proportionnalité. On divise le nombre de votes obtenus par le diviseur correspondant à ses sièges (ici on prend 5 pour 3 sièges), ce qui nous donne le quotient 4.8. On va ajouter des sièges aux autres partis, pour que 4.8 soit le plus faible quotient dans la méthode de Sainte-Lägue.



| Parti         | A       | B     | C   |
|:--------      |:-------:|------:| ---:|
| total         | 24      | 43    | 21  |
|:--------      |:-------:|------:| ---:|
| division par 1| 24      | 43    | 21  |
| division par 3| 8       | 14.3  | 7   |
| division par 5| 4.8     | 8.6   | 4.2 | 
| division par 7| 3.4     | 6.1   | 3   |
| division par 9| 2.7     | 4.9   | 2.3 | 
|=======================================|
| nb de sièges  | 3       | 5     | 2   |

On a donc ajouté 2 sièges de rééquilibrage au parti B et un au parti C afin de toujours respecter la proportionalité selon la méthode de Sainte-Lägue.


Effets de seuil, comment gérer les petits partis
=====

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

Pour remédier à ce problème il y a plusieurs solutions, les pays scandinaves utilisent une méthode de Sainte-Lägue modifiée au lieu d'imposer un seuil, en augmentant le premier diviseur, cela limite les partis de très petits taille sans générer d'effet de seuil indésirable. En Allemagne, le choix a été fait d'utiliser des quotas comme écrit plus haut, afin d'éviter les cas extrème comme l'exemple précédent, avant d'utiliser la méthode de Sainte-Lägue, on attribue un siège à chaque candidat·e indépendant·e qui a gagné son scrutin local. On réduit donc le nombre de sièges attribués par la méthode proportionelle.

Le principal problème du mode de scrutin allemand précédent est le nombre variant de déput·e·s élu·e·s. Lors des élections de 2023, il y a eu beaucoup trop de sièges attribués par compensation, et la taille du parlement (le batiment étant limitée, il a été décidé de changer de mode de scrutin).

Le nouveau mode de scrutin en Allemagne
=====
Lors des élections parlementaires allemandes en 2023, il y a eu 736 sièges attribués dont un grand nombre sont des sièges d'ajustement selon la méthode décrite plus haut. De nombreuses voix ont critiqué cette taille jugée déraisonable (non seulement il est difficile d'ajouter des sièges dans le batiment, mais il faut aussi payer les salaires des déput·e·s). Une réforme a donc été votée en 2023 qui supprime tout simplement les sièges attribués en compensations. Ainsi, un parti qui a plus de candidat·e·s élu·e·s localement que le nombre de sièges attribué par la méthode de Sainte-Lägue verra certain·e·s candidat·e·s directement élu·e·s ne pas avoir de sièges au parlement. C'est une réforme qui fait débat, certains partis d'opposition ayant un fort ancrage local sont contre car défavorisés par ce nouveau changement.


Les types d'élections parlementaires en Europe
=====

A partir de cet article et des précédents, on peut dégager plusieurs types d'élections parlementaires. La proportionelle globale utilise un scrutin au niveau national uniquement. Les scrutins par circonscription eux se basent sur des élections locales à un·e seul·e vainqueur·e. Entre les deux, on trouve les systèmes à la proportionelle par canton comme [celui de la IVème république](https://matthieuhervouin.github.io/posts/2012/08/blog-post-1/). Enfin, les proportionelles mixtes font un mélange des précédents comme dans le cas de l'Allemagne. Il y a plusieurs variantes de proportionelles mixtes, par exemple le Danemark fait un mélange entre proportionelle par canton et proportionelle globale.

Voici un résumé des différents systèmes utilisés pour les élections parlementaires en Europe, à noter que certains pays comme la Bosnie ou la Roumanie intègrent aussi des représentations des différentes ethnies dans leurs parlement.


| Type de scrutin                                                                                                           |
|===========================================================================================================================|
| Proportionnel global        | Italie, Pays-Bas, Grèce, République tchèque, Pologne                                        |
| Par circonscription         | France (Vème), Angleterre                                                                   |
| Proportionnel par canton    | France (IVème), Parlement européen, Espagne, Suisse, Autriche, Irlande, Roumanie            |
| canton + global             | Danemark, Norvège, Suède, Bosnie                                                            |
| circo + global              | Allemagne, Hongrie                                                                          |

| Règle utilisée                                                                                                            |
|===========================================================================================================================|
| D'Hondt                  | Danemark, Portugal, Espagne, Pays-Bas, République tchèque, Pologne, Autriche, Hongrie          |
| Sainte-Lägue             | Allemagne                                                                                      |
| Sainte-Lägue modifiée    | Suède, Norvège                                                                                 |
| Plus fort reste          | Italie, Suisse                                                                                 |
| Par classement           | Irlande                                                                                        |



Sources
=====
[vidéo rapide](https://youtu.be/azIpAiayPZY?si=itlPAeMglpNNZIax)

[Elections allemandes](https://fr.wikipedia.org/wiki/Élections_fédérales_allemandes_de_2021#Organisation)

[Page wiki en anglais](https://en.wikipedia.org/wiki/Electoral_system_of_Germany)

[Changement en 2023](https://www.dw.com/en/germany-passes-law-to-shrink-its-xxl-parliament/a-64471203)

[Ajustements en allemand](https://de.wikipedia.org/wiki/Sitzzuteilungsverfahren_nach_der_Wahl_zum_Deutschen_Bundestag#Sitzzuteilung_am_Beispiel_der_Bundestagswahl_2013)


