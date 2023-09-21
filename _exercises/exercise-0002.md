---
title: Exercice 2
position_number: 3
parameters:
  - name:
    content:
content_markdown: |-
  Créer une fonction en **PHP** qui va calculer **la moyenne d'un élève sur son premier trimestre** sachant qu'il n'a que **4 matières** : anglais, français, math et svt. Chaque trimestre il y'a **3 contrôles par matières**. Pour chaque contrôle c'est le **même coefficient** et c'est **noté sur 20**. Chaque matière est consituée d'un tableau de 3 notes.
  {: .info }
left_code_blocks:
  - code_block: |2-
    /** Première Version : Avec Boucle FOR **/
    function calcul_moyenne($anglais, $francais, $maths, $svt) {
      // Initialisation des variables pour stocker la somme des notes et le nombre total de notes
      $somme_notes = 0;
      $nombre_notes = 0;
      
      // Parcours du tableau des notes d'anglais et ajout des notes à la somme
      for ($i = 0; $i < 3; $i++) {
          $somme_notes += $anglais[$i];
          $nombre_notes++;
      }
      
      // Parcours du tableau des notes de français et ajout des notes à la somme
      for ($i = 0; $i < 3; $i++) {
          $somme_notes += $francais[$i];
          $nombre_notes++;
      }
      
      // Parcours du tableau des notes de mathématiques et ajout des notes à la somme
      for ($i = 0; $i < 3; $i++) {
          $somme_notes += $maths[$i];
          $nombre_notes++;
      }
      
      // Parcours du tableau des notes de SVT et ajout des notes à la somme
      for ($i = 0; $i < 3; $i++) {
          $somme_notes += $svt[$i];
          $nombre_notes++;
      }
      
      // Calcul de la moyenne en divisant la somme des notes par le nombre total de notes
      $moyenne = $somme_notes / $nombre_notes;
      
      // Renvoi de la moyenne calculée
      return $moyenne;
    }
    title: Solution 1
    language: php
  - code_block: |2-
    /** Deuxième Version : Avec Boucle FOREACH **/
    function calcul_moyenne($anglais, $francais, $maths, $svt) {
      // Initialisation des variables pour stocker la somme des notes et le nombre total de notes
      $somme_notes = 0;
      $nombre_notes = 0;
      
      // Parcours du tableau des notes d'anglais et ajout des notes à la somme
      foreach ($anglais as $anglaiss) {
        $somme_notes += $anglaiss;
        $nombre_notes++;
      }  
      // Parcours du tableau des notes de français et ajout des notes à la somme
      foreach ($francais as $francaiss) {
        $somme_notes += $francaiss;
        $nombre_notes++;
      }
      // Parcours du tableau des notes de mathématiques et ajout des notes à la somme
      foreach ($maths as $math) {
        $somme_notes += $math;
        $nombre_notes++;
      }
      // Parcours du tableau des notes de SVT et ajout des notes à la somme
      foreach ($svt as $svts) {
        $somme_notes += $svts;
        $nombre_notes++;
      }

      // Calcul de la moyenne en divisant la somme des notes par le nombre total de notes
      $moyenne = $somme_notes / $nombre_notes;
      
      // Renvoi de la moyenne calculée
      return $moyenne;
    }
    title: Solution 2
    language: php
right_code_blocks:
  - code_block: |-
      $anglais = [15, 16, 14]; // Tableau content les 3 notes en anglais pour un élève
      $francais = [17, 18, 16]; // Tableau content les 3 notes en français pour un élève
      $maths = [19, 20, 18]; // Tableau content les 3 notes en mathématiques pour un élève
      $svt = [14, 15, 13]; // Tableau content les 3 notes en svt pour un élève

      $moyenne_eleve = calcul_moyenne($anglais, $francais, $maths, $svt); // Appel de la fonction calcul_moyenne avec les 4 tableaux
      echo "La moyenne de l'élève est : " . $moyenne_eleve; // Affichage de la moyenne calculée
    title: Utilisation
    language: php
---