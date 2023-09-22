---
title: Exercice 4
position_number: 5
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui prend en argument un **nombre** et qui retourne **pair** si le nombre est pair et **impair** si le nombre est impair.
  {: .info }
left_code_blocks:
  - code_block: |-
      function pairOuImpair($nombre) {
        if ($nombre % 2 === 0) {
          // Si le reste de la division par 2 est égal à zéro, le nombre est pair
          return "pair";
        } else {
          // Sinon, le nombre est impair
          return "impair";
        }
      }
    title: Solution
    language: php
right_code_blocks:
  - code_block: |-
      $nombre_1 = pairOuImpair(4); // Appel de la fonction avec le nombre 4
      $nombre_2 = pairOuImpair(7); // Appel de la fonction avec le nombre 7
      echo "Le nombre est $nombre_1"; // Affichera "Le nombre est pair"
      echo "Le nombre est $nombre_2"; // Affichera "Le nombre est impair"
    title: Utilisation
    language: php
---