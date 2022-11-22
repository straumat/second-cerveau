---
title: "Données & pollution"
description: ""
date: 2022-11-22T17:32:57+01:00
lastmod: 2022-11-22T17:32:57+01:00
draft: false
images: []
type: docs
menu:
ressources:
parent: "sobriete-numerique"
identifier: "sobriete-numerique-donnees-et-pollution"
weight: 2
---

L’explosion des volumes provoquerait une explosion de la consommation électrique... c'est notamment une des raisons de
critiquer la 5G, puis la 6G (et tous les autres G précédents).

En fait, l’essentiel de la consommation électrique des réseaux est constitué par le fonctionnement de l’infrastructure,
indépendamment de la quantité de données.

Une ampoule LED consomme environ 8 watts, une ampoule incandescence 60 watts, à partir de cela, voici des éléments de
comparaisons:

- **Votre accès internet** : “la fibre consomme en moyenne un peu plus de 0,5 Watt par ligne, soit trois fois moins
  que l’ADSL (1,8W) et quatre fois moins que le RTC (2,1W) sur le réseau d’accès”. la partie concernant la transmission
  longue distance présente une consommation marginale par rapport à celle de la box qui représente aux alentours de 10 à
  30 watts suivant les générations.
- **Votre téléphone mobile** : Une batterie de téléphone mobile possède une capacité de 10 à 15 Wh. Une charge de
  téléphone
  mobile ne pourrait éclairer une ampoule que pendant 1 heure.
- **Le réseau
  mobile** : [Une étude finlandaise](https://www.researchgate.net/publication/326470455_Evaluating_the_Energy_Consumption_of_Mobile_Data_Transfer-From_Technology_Development_to_Consumer_Behaviour_and_Life_Cycle_Thinking)
  citée montre que la consommation électrique des opérateurs finlandais est restée à peu près stable pendant la décennie
  2010, malgré une légère croissance tendancielle (Alors que la croissance du volume explose). Le rapport ARCEP cité
  propose également une évaluation en termes de gaz à effet de serre montre une baisse progressive de l’empreinte des
  opérateurs français. Le développement de la 4G et 5G a permis au groupe Orange d'augmenter de 40% par an, depuis 2019,
  le trafic sur le mobile, sans accroître sa consommation d'énergie. Et depuis 2014, l'énergie requise pour transporter
  1 Go de data a été divisée par 10 (
  Voir [l'article du Figaro.](https://www.lefigaro.fr/secteur/high-tech/orange-s-organise-pour-faire-face-aux-coupures-d-electricite-20221109))
- **Les datacenters** : Une étude de l’agence internationale de l’énergie (IEA) montre, là encore, que la consommation
  électrique de ces centres n’explose pas, car les coûts principaux sont également des coûts fixes, et l’amélioration
  des équipements et de leur taux d’utilisation permet de traiter une quantité toujours croissante de services à
  consommation électrique égale.

On voit d’abord qu’aucun des éléments discutés, du serveur de données à notre téléphone, n’éprouve une sensibilité
particulière aux volumes de données échangés. Limiter les données n'a donc aucun sens, comme de limiter le nombre de
kilometres que vous pourriez faire en transport en commun.

Dans les travaux du Shift Project il existe des biais tellement évidents qu'ils décrédibilisent largement leur étude.
Ainsi, sur le poids du streaming : 80% de la consommation des réseaux est fixe et ne dépend pas de la charge du
réseau... Cela fausse tout leur raisonnement.

Sur l’“étude” du Shift Project, Carbon Brief avait publié un fact-check
par [George Kamiya](https://www.carbonbrief.org/factcheck-what-is-the-carbon-footprint-of-streaming-video-on-netflix)
qui s’est révélé vraiment violent avec des erreurs d’appréciation allant de 27× à 57×.

Il est tout simplement délirant d'envisager de multiplier par presque 3 l'empreinte des réseaux en 10 ans ; cela ne
tient pas compte du décommissionnement progressif de la 3 et 4G qui consomment beaucoup plus que la 5G.

**Sources**

- [La sobriété numérique, oui mais pour quoi faire ?](https://signal.eu.org/blog/2020/07/15/la-sobriete-numerique-oui-mais-pour-quoi-faire/)
