---
title: "Data engineering"
description: "Le Data Engineer définit, développe, met en place et maintient les outils et infrastructures adéquats à l'analyse de la donnée"
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

Le Data Engineer définit, développe, met en place et maintient les outils et infrastructures scalable nécessaires à
l'analyse de données. Le but de ce chapitre est de présenter les différents outils et technologies qui permettent de
mettre en place ce genre d'architecture.

## Dimensions de la donnée

On peut analyser de la donnée sous 4 angles différents :

- **Volume** : la quantité de données.
- **Vélocité** : la vitesse à laquelle les données sont produites.
- **Variété** : la diversité des formatés des données (structurées, non structurées, semi structurées).
- **Véracité** : la fiabilité des données, à quel point on peut lui faire confiance.

## Types de problèmes

### Problèmes de traitement

Ces problèmes rassemblent tout ce qui concerne la collecte des données, leur traitement et leur stockage.

Il y a 3 types de traitement :

- Les traitements temps réel qui sont généralement traités comme un flux de données auquel on réagit (de quelques
  secondes à 5 minutes). On utilise habituellement des bus de données ou d'évènements, car la capacité du consommateur
  doit être supérieur à la capacité du producteur d'évènement (Pub Sub framework).
- Les traitements en quasi-temps réel (de quelques minutes à une heure).
- Les traitements batchs qui sont des imports ou des générations de rapports (plus d'une heure). Au-dessus de 10 tera
  octets, on parle de Big Data.

### Problèmes de publication

La problématique ici est de publier les données aux bonnes personnes avec sécurité et une gouvernance adéquate des
données.

Il y a 3 types de publication :

- Les rapports qui sont des exports de données (tableaux de bord, rapports, etc.) qu'on peut réaliser avec
  elasticsearch+kibana ou Superset.
- Les API qui sont des interfaces de programmation qui permettent d'accéder aux données.
- Les référentiels de données de trois types : Data lake, Data wharehouse et Data mart.

## Stockage de données

### Formats de données

L'avantage des formats de données binaires est qu'ils sont plus légers que les formats textuels. Quand on ne sait pas
forcément le volume de données auquel s'attendre, il vaut mieux faire ce choix.

Apache Avro est un système de sérialisation de données open source qui permet de stocker et de transférer des données
entre différents systèmes et langages de programmation de manière efficace. Voici quelques raisons pour lesquelles vous
pourriez vouloir utiliser Apache Avro :

- **Performance** : Avro est conçu pour être extrêmement rapide et efficace en termes de traitement des données. Il peut
  gérer des volumes de données importants sans sacrifier les performances.
- **Portabilité** : Avro est conçu pour être utilisé avec une variété de langages de programmation. Cela signifie que
  vous pouvez facilement transférer des données entre différentes applications, même si elles sont écrites dans des
  langages différents.
- **Interopérabilité** : Avro prend en charge la définition de schémas de données. Cela permet à différents systèmes de
  communiquer entre eux en utilisant un schéma commun. Cela facilite la communication entre les systèmes et réduit les
  erreurs liées aux incompatibilités de données.
- **Compression** : Avro prend en charge la compression de données, ce qui peut réduire considérablement la quantité de
  données à stocker ou à transférer.
- **Évolution** : Avro prend en charge l'évolution des schémas de données au fil du temps. Cela signifie que vous pouvez
  ajouter de nouveaux champs à vos schémas de données sans casser les applications existantes.

### Stockage de données

Il existe trois types de stockage de données :

- Stockage de fichier : un fichier est créée, il a un nom et se trouve dans un dossier. Ceci ne permet pas de scaler ou
  de gérer de très gros fichiers.
- Stockage "blocs" : on découpe le fichier en blocs de taille fixe. On peut ensuite les stocker sur différents serveurs.
  Ceci permet de scaler en ajoutant des blocs. Le problème est que cela peut coûter assez cher et qu'il faut gérer les
  méta données. On trouve ce système dans la virtualisation comme avec Oracle VirtualBox.
- Stockage "objets" : les données sont stockées dans des conteneurs appelés objets qui ont un numéro unique ce qui
  permet une récupération et un stockage rapide. Cette solution est extrêmement scalable et la moins chère.

### Data lake, Data warehouse et Data mart

#### Data lake

Les data lake vont contenir les données provenant de diverses sources (applications, sites web, réseaux sociaux, base de
données, exports...) Ils vont servir de sources pour créer le data wharehouse et vont pouvoir aussi servir pour le
reporting, la data science ou le machine learning.

On peut y créer plusieurs zones :

- Raw data zone : Sources brutes.
- Master data zone : Données de références qui peuvent être utilisées pour enrichir les données brutes (ex : Open Data).
- User data zone : Données utilisateurs spécifiques.
- Curated data zone : Données nettoyées et structurées.
- Archive data zone : Données archivées.

#### Data warehouse

Les data wharehouse qui sont des bases de données qui contiennent des données consolidées et structurées utilisées pour
le reporting, l'analyse de données et la BI. En général un data wharehouse fait entre 100 giga octets et plusieurs tera
octets.

#### Data mart

Les data mart sont des bases de données qui contiennent des parties du data wharehouse qui concernent certains métiers.
En général un data mart ne dépasse pas les 100 giga octets.

## Base de données

### Types de base de données

Il existe 3 types de base de données :

- Base de données relationelles : elles sont structurées en tables et sont très performantes pour les requêtes
  complexes.
