# Mon second cerveau

Idées, inspirations, résumés de livres et d'articles sur différents sujets qui m'intéressent.

## Commandes principales

- Premier démarrage : `npm install`
- Ajouter un menu `npm run create -- --kind docs projets`.
- Ajouter une page `npm run create domaines/innovation/introduction/index.md`.

- Lancer le site web en local :

```bash
hugo serve
```

## Livres à résumer

- Clear thinking.
- Discipline is destiny.
- En toute franchise.
- Status and culture.
- Quand la machine apprend.
- La théorie du chaos (Ghys Etienne).
- Why information grows.
- La cité antique.
- How the world really works.
- La théorie des jeux démystifiée.

# Exporter la liste des titres

```bash
find ./content -type f -name "_index.md" -exec grep '^title:' {} \; | sed -e 's/- [ ] \(.*\)/\1/'
```

