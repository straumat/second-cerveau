---
title: "Les types de projets Open Source"
description: "Comment classer un projet Open Source ?"
date: 2022-11-22T09:52:18+01:00
lastmod: 2022-11-22T09:52:18+01:00
draft: false
images: []
type: docs
menu:
domaines:
parent: "open-source"
identifier: "open-source-types"
weight: 10
toc: true
---

On peut classer un projet open source avec quatre critères:

- **La portée technique** : Un projet qui semble avoir toutes les fonctionnalités requises attirera peu de nouveaux
  contributeurs. Il peut être très utilisé, mais il peut y avoir peu de choses à faire. Par exemple : Webpack.
- **Le besoin de support** : Le support correspond à répondre aux gens, traiter les demandes, relire le code des
  autres... Les contributeurs ont surtout envie d'écrire du code intéressant, pas de faire du triage de bugs. Par
  exemple, Youtube-dl est un projet assez simple avec peu de code, mais il y a énormément de demande de support.
- **La facilité de participation** : Quelle est la difficulté de contribuer à un projet pour un nouveau venu ? Est-ce un
  langage connu ? Est-ce bien documenté ? La communauté est-elle sympa ? les mainteneurs du projet sont ils disponibles
  ?
- **Nombre d'utilisateurs** : La portée du projet, c'est-à-dire quel est le potentiel de personnes qui pourraient être
  contributeurs ? Ceci est généralement une fonction du nombre de personnes qui pourraient utiliser l'application.

À partir de là, on se retrouve avec quatre grands types de projets:

- **Fédérations** : Ce sont des projets avec une croissance forte des utilisateurs et des contributeurs. On y trouve des
  projets comme Linux, Node.js ou Rust. Ces projets ressemblent à des entrepises et sont complexes à gérer ce qui les
  pousse à mettre en place des votes, des groupes de travail, des fondations...
- **Clubs** : Ce sont des projets avec une croissance forte des contributeurs, mais une croissance faible des
  utilisateurs. Astropy qui fournit des outils Python aux astronomes est un exemple. Ce projet va avoir peu
  d'utilisateurs, mais ceux-ci ont de bonnes chances de pouvoir être des contributeurs actifs. Ce sont un peu comme des
  meetups ou des associations.
- **Jouets** : Ce sont des projets avec peu de croissances des contributeurs et des utilisateurs. Ce sont des projets
  personnels. On a par exemple SSH-Chat qui permet à des utilisateurs de discuter via SSH.
- **Stades** : Ce sont des projets avec peu de croissance des contributeurs, mais une forte croissance des utilisateurs.
  Ils reçoivent bien quelques contributions, mais ce n'est rien comparé à la croissance des usages. On y trouve des
  projets comme Babel, Webpack, Bundler... Contrairement aux fédérations & clubs, le management est centralisé, on est
  sur du one to many.

Le futur des projets organisés autour communautés décentralisées (clubs & fédérations) réside dans le recrutement de
nouveaux contributeurs et la réduction de la friction sur leur recrutement. Les projets centralisés, eux, doivent
survivre avec moins de temps de contribution, les créateurs de ses projets essayent au maximum d'automatiser, de faire
faire le support de base par la communauté et d'éliminer toute "distraction".