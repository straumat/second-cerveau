---
title: "Les coûts d'un projet"
description: ""
date: 2022-11-22T09:52:18+01:00
lastmod: 2022-11-22T09:52:18+01:00
draft: false
images: []
type: docs
menu:
domaines:
parent: "open-source"
identifier: "open-source-cout-projet-open-source"
weight: 6
toc: true
---

Les deux premières choses dont il faut se rappeler:

- Un logiciel, une fois écrit, n'est jamais vraiment fini. Même si l'on vient à bout des fonctionnalités, il y a
  toujours une maintenance à faire. Fergus Henderson explique que chez Google, la plupart des logiciels sont
  régulièrement réécrits afin de les rendre plus simple et mieux réfléchi. Cela permet aussi de transférer les
  compétences.
- Un logiciel, une fois qu'il a un certain nombre d'utilisateurs, ne disparait jamais vraiment. Il continue de vivre
  très longtemps. Nous avons les exemples de Fortran, Cobol, NTP...

Malgré ces points, on a tendance à croire que les logiciels ont un cout marginal très faible, que produire le logiciel
coûte cher, mais que sa distribution ne coute quasiment rien. En gros, si je publie mon code sur Github, cela ne devrait
pas faire de différence si celui-ci est utilisé par une personne ou par un million de personnes. On va voir que cela
n'est pas le cas.

## Coûts marginaux

Le logiciel a deux propriétés qui nous font croire à un cout marginal nul:

- Pas de rivalité : si j'utilise un code téléchargé sir Github, je ne diminue pas la capacité d'une autre personne à
  utiliser ce même code pour ses besoins.
- Pas d'excluabilité : si quelqu'un a une copie, elle peut la distribuer à qui elle veut.

Ces deux propriétés ont tendance à faire penser que l'open source est un bien public, mais ce n'est pas tout à fait le
cas. De la même façon qu'ajouter des voitures sur une autoroute ne pose pas de problème jusqu'à ce qu'un embouteillage
se crée, plus on a d'utilisateurs sur un logiciel, plus on va avoir de travail "divers" à réaliser qui vont finir par
prendre beaucoup de temps.

## Support utilisateur

Quand un logiciel est peu utilisé, le coût du support est faible, mais cela peut vite changer. Dewitt Clinton de Google
présentait le problème de la façon suivante : "Si vous avez un milliard d'utilisateur que seul 0,1% ont besoin de
contacter le support une fois tous les trois ans pendant 10 minutes, cela vous coutera 19 années hommes chaque jour,
soit à peu près 21 000 personnes".

Le support des projets open source, ce ne sont pas le traitement des tickets, mais plutôt répondre aux questions
"comment ?" et "pourquoi ?".

Ceci implique aussi de passer du temps à faire de la modération comme on peut avoir à le faire sur Discord.

## Maintenance

Une étude de Stripe indique que les développeurs passent 48% de leur temps à maintenir du code.

## Refactoring

Plus le temps passe, plus vous ajouter de code, plus la dette technique augmente. Et en acceptant des contributions qui
peuvent avoir divers niveaux de qualité, on arrive parfois à un projet dont le code n'est pas uniforme. Le refactoring
est justement ce processus qui permet de rembourser la dette technique.

## L'adaptation aux besoins utilisateurs

Les besoins des utilisateurs vont aussi changer avec le temps, les mainteneurs vont devoir fournir un effort pour y
coller sous peine de voir la réputation du projet baisser ou éventuellement voir le projet mourir.


