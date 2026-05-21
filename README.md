# Suivi de budget PWA

Cette version est installable sur Android depuis un navigateur compatible PWA.

## Fonctions

- Définition du budget mensuel.
- Ajout, modification et suppression de dépenses.
- Ajout, modification et suppression de rentrées d’argent.
- Calcul automatique du budget restant selon la formule : budget + rentrées - dépenses.
- Recherche et tri des opérations.
- Réinitialisation des opérations en conservant le budget, ou remise à zéro complète.
- Export PDF via l’impression du navigateur.
- Sauvegarde et import JSON.
- Fonctionnement hors connexion après premier chargement.

## Fichiers inclus

- `index.html` : application complète.
- `manifest.webmanifest` : informations d’installation.
- `service-worker.js` : cache hors connexion.
- `icon-192.png` et `icon-512.png` : icônes de l’application.

## Test local sur ordinateur

Dans le dossier extrait, lancez un petit serveur local :

```bash
python3 -m http.server 8080
```

Puis ouvrez :

```text
http://localhost:8080
```

Le simple double-clic sur `index.html` ne suffit pas pour tester correctement l’installation PWA, car le service worker ne fonctionne pas en `file://`.

## Publication simple

Vous pouvez déposer ces fichiers sur GitHub Pages, Netlify, Cloudflare Pages ou tout hébergement HTTPS.

Sur Android :

1. Ouvrir l’adresse avec Chrome.
2. Menu Chrome.
3. Choisir « Ajouter à l’écran d’accueil » ou « Installer l’application ».

## Stockage

Les données sont stockées localement sur l’appareil via `localStorage`. L’application fonctionne aussi hors connexion après le premier chargement.

Le bouton « Sauvegarder » exporte un fichier JSON de sécurité.


## Installation Android en fenêtre autonome

Pour que l’application s’ouvre avec sa propre icône et sans onglet de navigateur, elle doit être servie depuis GitHub Pages en HTTPS, avec les fichiers `index.html`, `manifest.webmanifest`, `service-worker.js`, `icon-192.png` et `icon-512.png` à la racine du dépôt.

Après mise à jour du dépôt, ouvrez l’adresse GitHub Pages dans Chrome Android, puis utilisez le menu et choisissez « Installer l’application » ou « Ajouter à l’écran d’accueil ». Si une ancienne version existe déjà, supprimez d’abord l’ancien raccourci, puis videz les données du site dans Chrome si l’installation continue à ouvrir un simple onglet.
