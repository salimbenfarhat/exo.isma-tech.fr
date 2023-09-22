---
title: Exercice 7
position_number: 8
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui prend en argument **deux nombres** et qui retourne **le plus grand** des deux.
  {: .info }
left_code_blocks:
  - code_block: |2-
      /** Première Version **/
      function plusGrand($a, $b) {
        // Vérifie si $a est strictement supérieur à $b.
        if ($a > $b) {
          // Si c'est le cas, retourne $a comme le plus grand des deux.
          return $a;
        } else {
          // Sinon, retourne $b comme le plus grand des deux.
          return $b;
        }
      }
    title: Solution 1
    language: php
  - code_block: |2-
      /** Deuxième Version : Avec L'Opérateur Ternaire **/
      function plusGrand($a, $b) {
        // Utilisation de l'opérateur ternaire pour déterminer le plus grand des deux nombres.
        return ($a > $b) ? $a : $b;
      }
    title: Solution 2
    language: php
right_code_blocks:
  - code_block: |-
      // Déclaration de deux variables contenant les nombres à comparer.
      $a = 10;
      $b = 7;
      // Appel de la fonction plusGrand avec les deux nombres en arguments,
      // et stockage du résultat dans une variable appelée $resultat.
      $resultat = plusGrand($a, $b);
      // Affichage du résultat pour montrer quel nombre est le plus grand.
      echo "Le plus grand nombre entre $a et $b est $resultat.";
      // Affichera "Le plus grand nombre entre 10 et 7 est 10."
    title: Utilisation
    language: php
---
