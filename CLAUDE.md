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

## État au 18 novembre 2026

Deux blocs `class="todo"` sont encore dans la page et **visibles par les
visiteurs** :

- l'emplacement des témoignages
- **les deux boutons d'achat, qui pointent vers `#`**

Le troisième est bloquant pour un lancement. Tant qu'il est là, la page ne
devrait pas être indexée.
