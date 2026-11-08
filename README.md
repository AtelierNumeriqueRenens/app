# app

Page d'attente « site en chantier » de l'Association Réseau 4S, publiée avec GitHub Pages :
https://ateliernumeriquerenens.github.io/app/

## Contenu

- `index.html` : une page unique et autonome (HTML et CSS dans le même fichier, polices Google Fonts). Elle suit le thème clair ou sombre du système et porte une balise `noindex`, donc les moteurs de recherche ne l'indexent pas.
- `.github/workflows/deploy.yml` : le workflow de publication.

## Mettre à jour

1. Modifier `index.html`. Pour un aperçu local, il suffit de l'ouvrir dans un navigateur.
2. Faire un commit et un push sur `main`.

La barre d'avancement est fixée à 70 % à deux endroits : la largeur de `.bar i` dans le CSS et l'`aria-label` du bloc `.progress`. Il faut changer les deux.

## Déploiement

Chaque push sur `main` lance le workflow « Deploy to GitHub Pages ». On peut aussi le lancer à la main depuis l'onglet Actions (`workflow_dispatch`). La source GitHub Pages du dépôt est réglée sur « GitHub Actions ».

Il n'y a pas d'étape de build : le workflow publie la racine du dépôt telle quelle. Tout fichier ajouté ici, ce README compris, devient donc public sur le site. N'y mettez rien de privé.
