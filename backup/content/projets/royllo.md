---
title: Royllo
menuTitle: Royllo
---

### Détail du POC (Explorateur)



Quand on ajoute une donnée, cela crée une entrée dans la table UPDATES_ADD_ASSET qui "hérite" de la table "UPDATES".

Ensuite :

- Un batch va passer toutes les UPDATES qui sont à traiter.
- Il va décoder le genesis_bootstrap_info pour récupérer les informations de genèses (asset_id, meta...).
- La preuve doit permettre de valider que les informations de genèse sont inscrites dans l'une des feuilles de l'arbre.

Dans un deuxième temps:

- Permettre de se prouver que l'on est le "créateur" d'un asset.

### Marketing

