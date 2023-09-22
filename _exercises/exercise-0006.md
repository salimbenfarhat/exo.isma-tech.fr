---
title: Exercice 6
position_number: 7
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui va retourner la **période de la journée**(**matin**, **après-midi** ou **soir**) en fonction de l'**heure**.
  {: .info }
left_code_blocks:
  - code_block: |2-
      /** Première Version **/
      function periodeJournee($heure) {
        // Vérification si l'heure est en dehors de la plage valide (0-23).
        if ($heure < 0 || $heure > 23) {
          return "heure incorrecte";
        } elseif ($heure >= 5 && $heure < 12) {
          // Si l'heure est entre 5 (inclus) et 12 (exclus), c'est le matin.
          return "matin";
        } elseif ($heure >= 12 && $heure < 18) {
          // Si l'heure est entre 12 (inclus) et 18 (exclus), c'est l'après-midi.
          return "après-midi";
        } elseif ($heure >= 18 && $heure < 24) {
          // Si l'heure est entre 18 (inclus) et 24 (exclus), c'est le soir.
          return "soir";
        } else {
          // Sinon, c'est la nuit (pour les heures de 0 à 4).
          return "nuit";
        }
      }
    title: Solution 1
    language: php
  - code_block: |2-
      /** Deuxième Version : Avec L'Opérateur Ternaire **/
      function periodeJournee($heure) {
        // Utilisation de l'opérateur ternaire pour déterminer la période de la journée.
        return ($heure < 0 || $heure > 23) ? "heure incorrecte" : (($heure >= 5 && $heure < 12) ? "matin" : (($heure >= 12 && $heure < 18) ? "après-midi" : (($heure >= 18 && $heure < 24) ? "soir" : "nuit")));
      }
    title: Solution 2
    language: php
right_code_blocks:
  - code_block: |-
      $matin = 8; // Exemple d'heure valide pour le matin.
      $periodeMatin = periodeJournee($matin);
      echo "Nous sommes actuellement dans la période du $periodeMatin.";

      $apresmidi = 12; // Exemple d'heure valide pour l'après-midi.
      $periodeApresMidi = periodeJournee($apresmidi);
      echo "Nous sommes actuellement dans la période de l'$periodeApresMidi.";

      $soir = 16; // Exemple d'heure valide pour le soir.
      $periodeSoir = periodeJournee($soir);
      echo "Nous sommes actuellement dans la période du $periodeSoir.";

      $nuit = 2; // Exemple d'heure valide pour la nuit.
      $periodeNuit = periodeJournee($nuit);
      echo "Nous sommes actuellement dans la période de la $periodeNuit.";
    title: Utilisation
    language: php
---
