# noel-cadeaux

Petit site collaboratif pour organiser les cadeaux de Noël en famille.

- **Site en ligne :** https://nonsset.github.io/noel-cadeaux/
- **Fonctions :** listes de cadeaux par priorité, participations à plusieurs, budgets, représentation d'une autre personne, familles et filleul·es.
- **Technique :** un seul fichier `index.html` (HTML/CSS/JS), données dans Firebase Firestore (forfait gratuit), hébergement GitHub Pages.

## Fichiers
- `index.html` : le site. La configuration Firebase est en haut du fichier (elle n'est pas secrète).
- `firestore.rules` : les règles de sécurité à coller dans Firebase → Firestore → Règles.

## Accès
Chaque espace famille a un lien secret (`…/noel-cadeaux/#code`). Pas de mot de passe : toute personne qui a le lien peut voir et modifier les listes.
