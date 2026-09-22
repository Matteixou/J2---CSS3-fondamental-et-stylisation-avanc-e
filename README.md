# StreamFlix - Projet fil rouge CSS

## Objectif

Ce projet est une page web simple de plateforme de streaming fictive.
Le but est de styliser une structure HTML avec du CSS natif, en respectant une logique mobile-first et un design inspire de Netflix/Disney+.

## Fichiers du projet

- `index.html` : contient la structure de la page.
- `styles.css` : contient toute la mise en forme CSS.
- `screenshots-mobile.png`, `screenshots-tablet.png`, `screenshots-desktop.png` : captures utilisees pour verifier le responsive.

## Structure HTML

La page est organisee en trois grandes parties :

1. Un `header` avec le logo StreamFlix et la navigation.
2. Une section `.hero` avec un titre, un texte court et deux boutons.
3. Une section `.films` avec une grille de cartes de films.

Chaque film est represente par une carte `.card`, composee d'un faux poster, d'un titre et d'un genre.

## Logique CSS

Le CSS commence par une charte graphique dans `:root`.
Les variables permettent de garder une coherence sur les couleurs et les espacements :

```css
:root {
  --bg: #111;
  --card: #1f1f1f;
  --text: #fff;
  --muted: #bbb;
  --red: #e50914;
  --space: 20px;
}
```

La page utilise une identite visuelle sombre avec du rouge, ce qui rappelle les plateformes de streaming.

## Mobile-first

Le CSS est ecrit d'abord pour mobile.
Par defaut, la grille des films est sur une seule colonne :

```css
.grid {
  display: grid;
  grid-template-columns: 1fr;
}
```

Ensuite, des media queries adaptent la mise en page :

- a partir de `600px` : la grille passe en 2 colonnes.
- a partir de `900px` : la grille passe en 4 colonnes.

## Flexbox et Grid

Flexbox est utilise pour :

- aligner les liens de navigation ;
- centrer le texte dans les posters ;
- organiser le header sur tablette et ordinateur.

CSS Grid est utilise pour :

- creer une grille de films adaptable selon la taille de l'ecran.

## Effets visuels

Le projet utilise des effets simples :

- changement de couleur au survol des liens ;
- changement de fond au survol des boutons ;
- leger deplacement des boutons ;
- zoom discret des cartes de films.

Ces effets sont faits avec `transition`, `transform`, `:hover` et restent legers pour ne pas impacter les performances.

## Responsive teste

Le responsive a ete verifie avec trois tailles d'ecran :

- mobile : `390px`
- tablette : `768px`
- ordinateur : `1440px`

Les captures correspondantes sont presentes dans le projet.

## Branche Git

Le travail CSS a ete realise sur la branche :

```bash
cssNatif
```

## Lancer le projet

Il suffit d'ouvrir le fichier `index.html` dans un navigateur moderne.
Aucun serveur ou framework n'est necessaire.
