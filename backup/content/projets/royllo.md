---
title: Royllo
menuTitle: Royllo
---

### Taro et Royllo ? Qu'est-ce que c'est ?

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

### Quel est le plan à court terme ?

| Étape        | Livrables                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------|
| **Étape 1**  | ~~Première version de royllo.org indiquant nos objectifs~~                                        |
| _30/10/2022_ | Première version de learn.royllo.org présentant ce que l'on a compris                             |
|              | Faire la liste des communautés (Slack, Reddit, Github...) & comptes sur learn                     |
|              | Mise en place de mon compte Twitter Royllo pour échanger avec la communauté (changer le username) |
|              | Lancement officiel des deux sites                                                                 |
|              | ---                                                                                               |
| **Étape 2**  | Finaliser une version 0.1.0 de l'exlporateur                                                      |
| _30/12/2022_ | Lancement officiel de Taue                                                   |

### Détail du POC (Explorateur)

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

Quand on ajoute une donnée, cela crée une entrée dans la table UPDATES_ADD_ASSET qui "hérite" de la table "UPDATES".

Ensuite :

- Un batch va passer toutes les UPDATES qui sont à traiter.
- Il va décoder le genesis_bootstrap_info pour récupérer les informations de genèses (asset_id, meta...).
- La preuve doit permettre de valider que les informations de genèse sont inscrites dans l'une des feuilles de l'arbre.

Dans un deuxième temps:

- Permettre de se prouver que l'on est le "créateur" d'un asset.

### Marketing

On va suivre la stratégie définie dans le livre [The Embedded Entrepreneur](https://amzn.to/3LYWLWm).

- Plutôt que de partir sur l'explorateur d'univers complet qui parait compliqué, on part sur un premier produit explorer
  pour se faire connaître puis on développe la solution complète en parallèle.
- Faire la liste des communautés et des comptes Twitter.