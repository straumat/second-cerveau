---
title: "Comment marche ChatGPT ?"
description: ""
date: 2022-11-22T09:52:18+01:00
lastmod: 2022-11-22T09:52:18+01:00
draft: false
images: [ ]
type: docs
menu:
domaines:
parent: "data_et_ia"
identifier: "data_et_ia_data_engineering"
weight: 10
toc: true
---

Cet article a été écrit grâce à la lecture de [What Is ChatGPT Doing... And Why Does It Work?](https://amzn.to/48pD4Au).
Les images sont aussi issus de ce livre. Je vous recommande de le lire pour une explication plus détaillée et plus
précise.

## Introduction.

Comme cela a été expliqué à de nombreuses reprises, basiquement, ce que ChatGPT fait, c'est d'essayer de produire
un texte qui soit une suite de mots raisonnablement cohérents - Cohérent signifiant ici que le texte produit par le
modèle est similaire à ce que l'on pourrait attendre d'un humain qui aurait lu des millions de pages webs.

Le LLM que vous utilisez a lu des millions de pages webs. D'un point de vue très simplifié, s'il écrit "Le chat est"
et veut trouver le mot suivant dans sa phrase, il va regarder le mot qui vient le plus souvent après "Le chat est" dans
tout ce qu'il a lu et va le proposer. Cela va donner le mot "animal" par exemple - Bien sûr, il y avait d'autres
possibilités (mignon, félin...).

Fondamentalement, le système pour chaque mot se repose la question "étant donné le texte écrit jusqu'à présent, quel
devrait être statistiquement le prochain mot ?". L'idée est donc de créer un modèle qui permette d’estimer les
probabilités avec lesquelles des séquences de mots devraient se produire, même si ces séquences n'ont jamais été
explicitement vu dans le corpus de texte que nous avons donné au LLM.

## Qu'est-ce qu'un modèle ?

Imaginons, comme Galilée, que vous vouliez savoir combien de temps cela prend à un boulet de canon lâché d'un étage
particulier de la tour de Pise pour atteindre le sol. La solution la plus simple est de mesurer le temps que cela prend
pour chacun des étages.

L'autre façon de faire, c'est de modéliser le problème afin de trouver une fonction qui, à partir de paramètres (ici
l'étage de départ), va vous donner le temps que cela prend pour le boulet de canon de tomber. Nous allons donc commencer
par réaliser quelques mesures et les représenter sur un graphique :

![image](modelisation_etape_1.png)

La question est donc : à partir des mesures reportées sur le graphique ci-dessus, comment trouver une fonction qui va
nous donner la valeur pour les étages où nous n'avons pas de mesures ?
On peut commencer par tracer une droite qui passe au plus près de tous les points que nous avons mesurés :

![image](modelisation_etape_2.png)

La ligne droite donne un résultat qui est assez proche de la réalité, mais il y a des points qui sont un peu loin de la
droite. En essayant une formule mathématique plus compliquée (`a + b x + c x2`), on arrive à quelque chose de mieux :

![image](modelisation_etape_3.png)

Tout modèle que vous utilisez possède une structure sous-jacente particulière, puis un ensemble de paramètres que vous
pouvez définir pour qu'il colle le plus possible à vos attentes. Dans le cas de ChatGPT, il y a 175 milliards de
paramètres.

## Modéliser des tâches humaines.









