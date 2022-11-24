---
title: "Introduction"
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
    identifier: "royllo-introduction"
weight: 1
toc: true
---

Le protocole « Taro » (Taproot Asset Representation Overlay) permet aux gens d'émettre des actifs numériques sur la
blockchain Bitcoin (comme un stablecoin ou un NFT). Ces actifs peuvent être transférés avec une transaction Bitcoin
classique ou une transaction hors chaîne sur le Lightning Network.

[Royllo](https://www.royllo.org/) est mon nouveau "projet du week-end", il s'agit de travailler sur des solutions qui
peuvent faciliter l'adoption du protocol Taro. Le projet se compose de plusieurs composants :

- Un site web public détaillant ce qu'on veut faire
- Un site web destiné aux débutants et qui décrit le fonctionnement de Taro et comment le mettre en œuvre
- Un explorateur des assets déclarés sur la chaîne.
- Une solution Open Source permettant d'explorer
  des [univers Taro](https://github.com/Roasbeef/bips/blob/bip-taro/bip-taro-universe.mediawiki) : Taue
- Une librairie common qui doit permettre de manipuler les concepts Taro en Java
