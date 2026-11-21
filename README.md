# Hisense Dashboard — prototype v0.1

Prototype web autonome du tableau de bord demandé pour Hisense 58A6FG / MTK9602 / VIDAA U9.

## Ce que fait cette version
- Écran d'accueil 16:9 inspiré de la capture de référence.
- Horloge et date locales.
- Météo par ville saisie manuellement (géocodage + météo Open-Meteo).
- Tuiles de raccourcis vers des sites web.
- Champ facultatif pour l'URL d'un serveur Jellyfin.
- Réglages enregistrés dans le stockage local du navigateur.
- Navigation de base avec les flèches directionnelles et OK.

## Ce qui n'est PAS implémenté
- Lancement des applications natives VIDAA.
- Commutation HDMI ou lecture de l'état des entrées.
- Remplacement du bouton HOME / du lanceur natif.
- Intégration API Jellyfin (les identifiants et la bibliothèque ne sont pas encore gérés).
- Installation garantie comme application VIDAA.

Les tuiles Netflix, YouTube, Prime Video et Disney+ ouvrent des pages web. Le support de lecture de ces sites dans le navigateur VIDAA n'est pas garanti.

## Déploiement sans serveur domestique
Ce prototype est un site statique. Il peut être hébergé sur un hébergement statique HTTPS (par exemple GitHub Pages) : aucun PC, NAS ou Raspberry Pi n'a besoin de rester allumé chez toi. La météo requiert Internet.

1. Crée un dépôt GitHub vide nommé `hisense-dashboard`.
2. Décompresse cette archive et téléverse `index.html` et `README.md` à la racine du dépôt.
3. Dans Settings > Pages, choisis le déploiement depuis la branche `main`, dossier `/root`.
4. Attends l'URL HTTPS fournie par GitHub Pages.
5. Depuis le navigateur de la TV, ouvre cette URL pour le premier essai.

## Installation dans DevKit
La documentation publique VIDAA décrit un App Manager qui installe une application web à partir d'une URL, mais cette opération peut demander une autorisation / secure code propre au téléviseur. Ne partage pas ton Device Code, MAC, numéro de série ou secure code ici.
Ne tente pas de contourner cette autorisation. Si App Manager est accessible et autorisé, utilise uniquement l'URL HTTPS du site statique, un nom d'application `Hisense Dashboard`, et une icône hébergée publiquement. Sinon, garde le test dans le navigateur de la TV.

## Retour arrière
- Test navigateur : quitter le navigateur avec la touche Back/Home.
- Application installée via DevKit : utiliser App Manager pour désinstaller `Hisense Dashboard` si cette option est disponible.
- Aucun firmware, partition système ou réglage de démarrage n'est modifié par ce prototype.

## Confidentialité
La ville météo est conservée localement dans le navigateur. La requête de géocodage et météo est envoyée à Open-Meteo. Aucun compte n'est requis. Ne saisis pas d'informations personnelles.
