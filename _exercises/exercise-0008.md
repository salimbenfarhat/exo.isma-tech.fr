---
title: Exercice 8
position_number: 9
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui prend en argument un **tableau de nombres** et qui retourne la **somme de ces nombres**.
  {: .info }
left_code_blocks:
  - code_block: |-
      function sommeTableau($tableau) {
        // Initialise une variable pour stocker la somme.
        $somme = 0;
        // Parcourt le tableau et ajoute chaque nombre à la somme.
        foreach ($tableau as $nombre) {
          $somme += $nombre;
        }
        // Retourne la somme calculée.
        return $somme;
      }
    title: Solution
    language: php
right_code_blocks:
  - code_block: |-
      $mesNombres = [10, 20, 30, 40, 50];
      $resultat = sommeTableau($mesNombres);
      echo "La somme des nombres est : $resultat"; // Affichera "La somme des nombres est : 150"
    title: Utilisation
    language: php
---
