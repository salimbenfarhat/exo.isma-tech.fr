---
title: Exercice 3
position_number: 4
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui va retourner de quelle **type de personne** il s'agit(**un enfant**, **un jeune**, **un adulte** ou **une personne agée**) en fonction de son **age**.
  {: .info }
left_code_blocks:
  - code_block: |2-
      /** Première Version **/
      function getTypePersonne($age) {
        if ($age < 0) { // Si l'âge est inférieur à 0
          return "Age invalide"; // Retourne "Age invalide"
        } elseif ($age < 18) { // Sinon si l'âge est compris entre 0 et 18 ans (non inclus)
            eturn "Enfant"; // Retourne "Enfant"
        } elseif ($age < 30) { // Sinon si l'âge est compris entre 18 et 30 ans (non inclus)
          return "Jeune"; // Retourne "Jeune"
        } elseif ($age < 60) { // Sinon si l'âge est compris entre 30 et 60 ans (non inclus)
          return "Adulte"; // Retourne "Adulte"
        } elseif ($age < 100) { // Sinon si l'âge est compris entre 60 et 100 ans (non inclus)
          return "Personne agée"; // Retourne "Personne agée"
        } else { // Sinon (si l'âge est supérieur ou égal à 100 ans)
          return "Centenaire ou plus"; // Retourne "Centenaire ou plus"
        }
      }
    title: Solution 1
    language: php
  - code_block: |2-
      /** Deuxième Version **/
      function getTypePersonne($age) {
        if ($age < 18) { // Si l'âge est inférieur à 18 ans
          if ($age < 0) { // Si l'âge est inférieur à 0
            return "Age invalide"; // Retourne "Age invalide"
          } else {
            return "Enfant"; // Sinon retourne "Enfant"
          }
        } elseif ($age < 30) { // Sinon si l'âge est compris entre 18 et 30 ans (non inclus)
          return "Jeune"; // Retourne "Jeune"
        } elseif ($age < 60) { // Sinon si l'âge est compris entre 30 et 60 ans (non inclus)
          return "Adulte"; // Retourne "Adulte"
        } elseif ($age < 100) { // Sinon si l'âge est compris entre 60 et 100 ans (non inclus)
          return "Personne agée"; // Retourne "Personne agée"
        } else { // Sinon (si l'âge est supérieur ou égal à 100 ans)
          return "Centenaire ou plus"; // Retourne "Centenaire ou plus"
        }
      }
    title: Solution 2
    language: php
right_code_blocks:
  - code_block: |-
      echo getTypePersonne(-1); // Retourne "Age invalide"
      echo getTypePersonne(17); // Retourne "Enfant"
      echo getTypePersonne(18); // Retourne "Jeune"
      echo getTypePersonne(30); // Retourne "Adulte"
      echo getTypePersonne(70); // Retourne "Personne agée"
      echo getTypePersonne(110); // Retourne "Centenaire ou plus"
    title: Utilisation
    language: php
---