---
title: Exercice 1
position_number: 2
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui prend 3 paramètres : **un signe**, **une valeur 1** et **une valeur 2**. Cette fonction permettra de faire une **addition**, **soustraction**, **multiplication** ou **division** lorsque l'on appelle cette fonction.
  {: .info }
left_code_blocks:
  - code_block: |2-
      /** Première Version : Avec IF / ELSE **/
      function calcul($signe, $valeur1, $valeur2) {
          // Vérifie le signe fourni
          if ($signe == '+') {
              // Si le signe est +, renvoie la somme des deux valeurs
              return $valeur1 + $valeur2;
          } else if ($signe == '-') {
              // Si le signe est -, renvoie la différence des deux valeurs
              return $valeur1 - $valeur2;
          } else if ($signe == '*') {
              // Si le signe est *, renvoie le produit des deux valeurs
              return $valeur1 * $valeur2;
          } else if ($signe == '/') {
              // Si le signe est /, vérifie si la valeur 2 est égale à 0 pour éviter une division par zéro
              if ($valeur2 == 0) {
                  // Si la valeur 2 est égale à 0, renvoie un message d'erreur indiquant une division par zéro
                  return "Erreur : division par zéro";
              } else {
                  // Sinon, renvoie le quotient des deux valeurs
                  return $valeur1 / $valeur2;
              }
          } else {
              // Si aucun de ces cas n'est vérifié, renvoie un message d'erreur indiquant que le signe n'est pas reconnu
              return "Erreur : signe non reconnu";
          }
      }
    title: Solution 1
    language: php
  - code_block: |2-
      /** Deuxième Version : Avec SWITCH / CASE  **/
      function calcul($signe, $valeur1, $valeur2) {
          // Vérifie le signe fourni
          switch ($signe) {
              case '+':
                  // Si le signe est +, renvoie la somme des deux valeurs
                  return $valeur1 + $valeur2;
              case '-':
                  // Si le signe est -, renvoie la différence des deux valeurs
                  return $valeur1 - $valeur2;
              case '*':
                  // Si le signe est *, renvoie le produit des deux valeurs
                  return $valeur1 * $valeur2;
              case '/':
                  // Si le signe est /, vérifie si la valeur 2 est égale à 0 pour éviter une division par zéro
                  if ($valeur2 == 0) {
                      // Si la valeur 2 est égale à 0, renvoie un message d'erreur indiquant une division par zéro
                      return "Erreur : division par zéro";
                  } else {
                      // Sinon, renvoie le quotient des deux valeurs
                      return $valeur1 / $valeur2;
                  }
              default:
                  // Si aucun de ces cas n'est vérifié, renvoie un message d'erreur indiquant que le signe n'est pas reconnu
                  return "Erreur : signe non reconnu";
          }
      }
    title: Solution 2
    language: php
right_code_blocks:
  - code_block: |-
      echo calcul('+', 3, 4); // Affiche 7  
      echo calcul('-', 5, 2); // Affiche 3  
      echo calcul('*', 6, 7); // Affiche 42  
      echo calcul('/', 8, 2); // Affiche 4  
      echo calcul('/', 9, 0); // Affiche "Erreur : division par zéro"  
      echo calcul('^', 2, 3); // Affiche "Erreur : signe non reconnu"
    title: Utilisation
    language: php
---