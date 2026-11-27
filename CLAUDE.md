# Règles du dépôt noel-cadeaux

- Langue : tout en français (interface, commits, pull requests, documentation).
- Le site est un seul fichier `index.html`, sans dépendance ni compilation. Ne pas introduire de framework.
- À chaque évolution visible :
  1. incrémenter `APP_VERSION` dans `index.html` ;
  2. ajouter une section en haut de `CHANGELOG.md` (date, liste courte des nouveautés en langage simple) ;
  3. mettre à jour `README.md` si les fonctions ou la version changent ;
  4. mettre à jour l'aide intégrée (`HELP` dans `index.html`) si une page change.
- Travailler sur une branche, ouvrir une pull request vers `main`, puis fusionner : GitHub Pages republie `main`.
- Tester en mode démo (copie avec `window.FIREBASE_CONFIG = null`) avant de publier.
- Confidentialité à respecter : on ne doit jamais voir les participations à ses propres cadeaux, ni les surprises hors liste qui nous concernent, y compris quand on agit pour une personne représentée.
- Une mise à jour ne doit jamais effacer ni masquer les données existantes : nouveaux champs facultatifs, pas de renommage de collection ou de champ sans migration, et tester qu'un espace créé avec la version précédente s'ouvre toujours.
- Toute valeur venant de la base est échappée (`esc`) avant d'être insérée dans le HTML.
