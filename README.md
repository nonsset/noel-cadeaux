# noel-cadeaux

Petit site collaboratif pour organiser les cadeaux de Noël en famille.

- **Site en ligne :** https://nonsset.github.io/noel-cadeaux/
- **Version actuelle :** 1.3 — voir les [notes de version](CHANGELOG.md)
- **Support :** nonsset@gmail.com (aussi accessible depuis le bouton « Aide » du site)

## Ce que fait le site
- Chacun fait sa liste de cadeaux, classée par ordre de préférence.
- Chacun participe à un ou plusieurs cadeaux des autres (montant, « c'est moi qui achète », petit mot), jamais aux siens.
- Surprise préservée : on ne voit ni qui participe à ses cadeaux, ni combien, ni les surprises hors liste qu'on nous prépare.
- Budget maximum par personne.
- On peut représenter une personne qui n'utilise pas le site (ex. une grand-mère).
- Familles (une personne peut être dans plusieurs) et filleul·es.
- Code personnel à la connexion, et un rôle d'organisateur pour faire le ménage (doublons, codes oubliés).
- Aide intégrée sur chaque page.

## Technique
- Un seul fichier `index.html` (HTML, CSS, JavaScript), sans étape de compilation.
- Données dans **Firebase Firestore** (forfait gratuit Spark). La configuration Firebase est en haut de `index.html` : elle n'est pas secrète.
- Hébergement **GitHub Pages** depuis la branche `main` : chaque fusion dans `main` met le site à jour en une à deux minutes.
- `firestore.rules` : copie des règles de sécurité publiées dans Firebase → Firestore → Règles.
- Sans configuration Firebase (`window.FIREBASE_CONFIG = null`), le site tourne en **mode démo** avec des données d'exemple stockées dans le navigateur.

## Accès et sécurité
Chaque espace famille a un lien secret (`…/noel-cadeaux/#code`) et chacun a un code personnel. Chaque appareil mémorise les espaces déjà ouverts : l'adresse simple du site ramène au dernier utilisé.
Ces protections sont faites dans l'interface et suffisent dans un cercle familial. Une personne qui a le lien et des connaissances techniques pourrait toutefois lire les données directement.
