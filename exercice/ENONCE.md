# Exercice 7 : Finaliser le thème alternatif

<!--
SI TU UTILISES UN ÉDITEUR CAPABLE DE PRÉVISUALISER MARKDOWN,
FAIS-LE.  PAR EXEMPLE, DANS VS CODE, CMD/CTRL+SHIFT+V AFFICHE LA PRÉVISUALISATION.
-->

Toi aussi tu n’aimes pas laisser un truc en plan ? Lorsqu’on a décliné le thème de Noël, on n’est pas allé au bout : seuls certains boutons, navigations et l’icône Twitter ont été mis à jour.

Il reste tous les autres icônes et un paquet de CSS (ex. `example`, `button`, `glide-theme`, `image`, `section`…) avec, du coup, leurs variables de couleurs et leurs variations dans le thème (y compris la déclinaison « en dur » pour IE 11).

## Résultat attendu

[La maquette](./RESULTAT_ATTENDU.png) est là.

## Tâches de cet exercice

1. Pour chaque feuille de style composant qui n’est pas déjà « thémée » (ex. `button`, `example`, `glide-theme`, `image`, `section`, `testimony`) :
   - Recense les codes couleurs qui doivent être thémés, et pour chacun :
     - Recherche dans `_settings.color.scss` si la couleur existe, sinon ajoute-la ;
     - Au même endroit, recherche si l’alias « sémantique » de couleur existe, sinon ajoute-le ;
     - Remplace la couleur en dur par une référence à la _custom property_ ainsi définie ;
     - Effectue les mêmes manip’s pour les réglages couleurs du thème de Noël.

- Retranscris ces modifications, avec les couleurs de Noël en dur, dans `themes/_theme.christmas.scss` pour la compatibilité IE 11.

2. Pour chaque icône au-delà de celle de Twitter (ex. `back-to-top`, `comment`, `maintenance`, `operational`, `responsive`, `scalable`, `testimonies`) :
   - Modifie sa source (dans `assets/svg`) pour utiliser un `fill="currentColor"` ;
   - S’il était utilisé en image de fond : retire ça de la CSS et injecte-le avec les bonnes classes (généralement `c-section__img` ou `o-media__img`…) ;
   - S’il était déjà présent _inline_ par référence au fichier `img/sprite.svg` externe, remplace-le par un `<svg>` en ligne avec les mêmes classes et un `<use xlink:href="#…"></use>` approprié à l’intérieur.
     - Si un `alt=` était présent sur l’`<img>`, il peut être remplacé par un `<title id="…">…</title>` dans le `<svg>` en ligne, référencé depuis l’attribut `aria-labelledby` de ce `<svg>`.
