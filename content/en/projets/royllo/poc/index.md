---
title: "POC"
description: ""
lead: ""
date: 2022-01-25T14:41:39+01:00
lastmod: 2022-01-25T14:41:39+01:00
draft: false
images: []
type: docs
menu:
projets:
parent: "royllo"
identifier: "royllo-poc"
weight: 3
toc: true
---

Il s'agit d'une application web déployée sur explorer.royllo.org/test.

Elle ressemble à l'écran Google:

- Une page d'accueil qui renvoie vers /test.
- Un champs de recherche pour trouver des assets (recherche sur nom & metadata pour le moment):
    - Une page qui liste les résultats.
    - Une page d'affichage d'un asset en popup quand on clique dessus.
- Un bouton "Add Asset" en haut à droite où je peux envoyer un genesis_bootstrap_info, une preuve et éventuellement les
  métas > Un numéro identifiant est retourné avec un lien vers la page des updates.
- Un bouton "API" qui détaille l'API et présente un exemple d'appel.
- Un bouton "Updates" qui liste les 50 dernières updates et leurs statuts (+ pagination).
- Un bouton contact.