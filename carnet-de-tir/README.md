# Carnet de Tir

Carnet de tir à l'arc qui s'installe sur iPhone (et Android) depuis le navigateur : saisie des flèches sur blason avec loupe, feuille de marque, historique et statistiques (progression, répartition des impacts, groupement).

Blasons : trispot 40 cm, 40 cm, 80 cm réduit (5–10), 80 cm, 122 cm, cible 3D (11/10/8/5).

L'application fonctionne hors ligne une fois installée. Les séances sont enregistrées sur l'appareil, dans le stockage du navigateur.

## Mise en ligne avec GitHub Pages

1. Crée un dépôt public sur GitHub, par exemple `carnet-de-tir`.
2. Envoie tout le contenu de ce dossier à la racine du dépôt (bouton **Add file → Upload files**, ou `git push`). Le fichier `.nojekyll` doit être inclus.
3. Dans le dépôt : **Settings → Pages**, section *Build and deployment* : *Source* = **Deploy from a branch**, branche **main**, dossier **/ (root)**, puis **Save**.
4. Après une ou deux minutes, le site est disponible à l'adresse `https://<ton-identifiant>.github.io/carnet-de-tir/`.

## Installation sur iPhone

1. Ouvre l'adresse du site dans **Safari**.
2. Touche le bouton **Partager**, puis **Sur l'écran d'accueil**, puis **Ajouter**.
3. Lance l'application depuis son icône : elle s'ouvre en plein écran et fonctionne sans réseau.

Ouvre-la toujours depuis l'icône : l'application installée et Safari ont chacun leur propre stockage, donc des séances différentes.

## Sauvegarde des séances

Les données restent sur le téléphone. Si tu supprimes l'icône de l'écran d'accueil, elles sont effacées.
Onglet **Historique → Sauvegarde** : *Exporter* copie toutes les séances sous forme de texte (à garder dans Notes ou un mail), *Importer* les restaure. Cela permet aussi de transférer les séances entre la version Android, la version en ligne et l'iPhone.

## Mettre à jour l'application

1. Remplace `index.html` (et les autres fichiers modifiés) dans le dépôt.
2. Dans `sw.js`, augmente `VERSION` (par exemple `1.0.1`). Sans ça, les iPhone gardent l'ancienne version en cache.
3. Sur l'iPhone, ouvre l'application avec du réseau, ferme-la complètement puis rouvre-la : la nouvelle version est chargée. Les séances sont conservées.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | L'application complète (HTML, CSS, JavaScript) |
| `manifest.webmanifest` | Nom, icônes et mode plein écran pour l'installation |
| `sw.js` | Mise en cache pour le fonctionnement hors ligne |
| `icons/` | Icône d'écran d'accueil (iPhone et Android) |
| `.nojekyll` | Indique à GitHub Pages de servir les fichiers tels quels |
