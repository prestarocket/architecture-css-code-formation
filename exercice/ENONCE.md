# Exercice 5 : Corriger un bug sur Edge

<!--
SI TU UTILISES UN ÉDITEUR CAPABLE DE PRÉVISUALISER MARKDOWN,
FAIS-LE.  PAR EXEMPLE, DANS VS CODE, CMD/CTRL+SHIFT+V AFFICHE LA PRÉVISUALISATION.
-->

Les choix d’intégration que nous avons fait pour les pavés de couleurs en haut au centre du pied de page, qui utilisent notamment une translation horizontale, entraînent un bug répertorié sur IE qui affiche un ascenseur horizontal en bas de la fenêtre.

Les commentaires conditionnels n’étant plus exploitables sur IE depuis IE 10, nous ne pouvons pas juste inclure une CSS conditionnellement, et devons recourir à un hack.

## Résultat attendu

[La maquette](./RESULTAT_ATTENDU.png) est là.

## Tâches de cet exercice

1. Ajoute une classe `_c-footer` (préfixe conventionnel `_` de hack) dans le HTML sur l’élément approprié.
2. Dans `_components.footer.scss` :
   - Ajoute le correctif (un simple `overflow-x: hidden`).
   - Injecte au-dessus du correctif un commentaire d’info renseignant l'objet de ce dernier.
