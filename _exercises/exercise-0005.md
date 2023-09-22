---
title: Exercice 5
position_number: 6
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui prend en argument un **nombre** et qui retourne **positif** si le nombre est positif, **négatif** si le nombre est négatif et **null** si le nombre est nul.
  {: .info }
left_code_blocks:
  - code_block: |-
      function positifNegatifOuNul($nombre) {
        if ($nombre > 0) {
          // Si le nombre est supérieur à zéro, il est positif
          return "positif";
        } elseif ($nombre < 0) {
          // Si le nombre est inférieur à zéro, il est négatif
          return "négatif";
        } else {
          // Sinon, le nombre est nul
          return "nul";
        }
      }
    title: Solution
    language: php
right_code_blocks:
  - code_block: |-
      $nombre_1 = positifNegatifOuNul(-3); // Appel de la fonction avec le nombre -3
      $nombre_2 = positifNegatifOuNul(0); // Appel de la fonction avec le nombre 0
      $nombre_3 = positifNegatifOuNul(5); // Appel de la fonction avec le nombre 5
      echo "Le nombre est $nombre_1"; // Affichera "Le nombre est négatif"
      echo "Le nombre est $nombre_2"; // Affichera "Le nombre est nul"
      echo "Le nombre est $nombre_3"; // Affichera "Le nombre est positif"
    title: Utilisation
    language: php
---