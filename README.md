# Suivi de budget PWA

Cette version est installable sur Android depuis un navigateur.

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
