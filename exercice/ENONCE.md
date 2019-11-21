# Exercice 4 : Assujettir le picto Twitter au thème

<!--
SI TU UTILISES UN ÉDITEUR CAPABLE DE PRÉVISUALISER MARKDOWN,
FAIS-LE.  PAR EXEMPLE, DANS VS CODE, CMD/CTRL+SHIFT+V AFFICHE LA PRÉVISUALISATION.
-->

Le thème est bien joli, mais le pictogramme Twitter reste de la même couleur quoiqu’il arrive, c’est tout de même dommage !

Cet icône est pour le moment affiché par un arrière-plan CSS, mais ça ne va pas nous permettre de l’assujettir au thème, il va donc falloir en faire une image _inline_ dans le contenu. Pour cela, on va s'appuyer sur l'objet `media` créé pour mettre en vis à vis les pictos et les contenus de la section « Principaux avantages », sauf qu’il faudra ajuster la marge et la dimensions des icônes.

## Résultat attendu

[La maquette](./RESULTAT_ATTENDU.png) est là.

## Tâches de cet exercice

1. Lis le contenu du fichier [`helpers/inline-svg.html`](../helpers/inline-svg.html).
2. Ajuste l’attribut `fill=` de [`assets/svg/twitter.svg`](assets/svg/twitter.svg) pour utiliser la valeur réservée `currentColor` (basée sur la couleur de texte en vigueur dans le contexte d’exploitation) plutôt que le blanc en dur.
3. Copie-colle le premier bloc juste après l’ouverture du `<body>` dans `index.html`, et remplace le pseudo-SVG imbriqué par le contenu de ton `build/sprite.svg`.
4. Ajuste le balisage et les styles du composant `.c-footer__list-item` pour utiliser plutôt un média calé à gauche, comme dans la section « Principaux avantages ».
5. Ajoute une variable sémantique d’alias (la couleur de base est déjà définie) à ton thème de Noël pour le picto Twitter, et utilise-la dans une règle adaptée pour que ton icône prenne la couleur attendue. Et voilà !

## Astuces

- N'oublie pas d'exprimer les dimensions et les espaces en unité relative (`rem`).
