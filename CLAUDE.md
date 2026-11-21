# Ce dossier est la page de vente EN LIGNE

`index.html` n'est pas un brouillon. C'est le fichier servi sur
**sonar.stupid-seller.com**, via GitHub et Netlify.

## Après toute modification de index.html ou de img/

Pousse, sinon la modification reste sur ce poste et le site en ligne garde
l'ancienne version :

```bash
git add -A && git commit -m "ce que tu as changé" && git push
```

Netlify reconstruit tout seul, le site est à jour en une trentaine de secondes.

## Pourquoi cette règle existe

Deux sessions Claude ont travaillé sur cette page en parallèle les 17 et
18 novembre, sur deux copies différentes. Elles ont divergé, et une partie du
travail a failli être écrasée. Il n'y a plus qu'un seul fichier, mais ça ne
suffit pas : il faut aussi que chacun pousse ce qu'il change.

## Ce qui n'est pas déployé

`PRODUCT.md`, `index.before-impeccable.html` et les instantanés `index.round*`
sont dans `.gitignore`. Ils restent en local. Ne les suis pas dans Git, ils
seraient publiquement accessibles.

Ce `CLAUDE.md` est suivi dans Git mais n'est pas servi : la commande de build
de `netlify.toml` le supprime avant la mise en ligne. Garde cette commande.

## État au 21 novembre 2026

- Le bouton de la carte 199 € pointe vers le paiement ThriveCart
  https://stupid-seller.thrivecart.com/sonar/ . Les autres boutons « Je prends
  Le Sonar » renvoient vers l'offre (#offre).
- Le bouton 399 € (« Je prends la validation ») pointe vers
  https://stupid-seller.thrivecart.com/sonar-rel/ .
- Plus aucune note interne (`class="todo"`) n'est visible sur la page.
- À minuit le 29 novembre, la page passe seule à 299 € ; le prix ThriveCart
  doit être changé au même moment, côté ThriveCart.
