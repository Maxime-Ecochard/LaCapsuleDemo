# Capsule Vidéo pour le Rétablissement 💙

[![PWA](https://img.shields.io/badge/PWA-Ready-blue.svg)](https://web.dev/progressive-web-apps/)
[![Privacy](https://img.shields.io/badge/Privacy-Local_Only-green.svg)](#confidentialité-et-sécurité)

**Capsule Vidéo pour le Rétablissement** est une application web progressive (PWA) conçue pour aider les personnes à enregistrer leurs **Directives Anticipées en Psychiatrie (DAP)** sous format vidéo. 

L'objectif est de permettre aux utilisateurs d'exprimer leurs souhaits de soin et leurs ressources en cas de crise, afin que leur voix soit entendue même lorsqu'ils ne sont plus en mesure de s'exprimer.

## ✨ Fonctionnalités Clés

- **📝 Aide à la rédaction** : Un outil dédié pour préparer son script avec des points de repère et des conseils pédagogiques.
- **📹 Enregistreur avec téléprompteur** : Enregistrez votre vidéo tout en lisant votre script directement sur l'écran. Navigation facile entre les sections.
- **🔒 Sécurité Maximale** : Toutes les vidéos et données personnelles sont chiffrées localement sur votre appareil. Rien ne transite par un serveur.
- **📱 Installation PWA** : Utilisable comme une application native sur iPhone et Android, même hors connexion.
- **📂 Gestion des versions** : Conservez votre capsule actuelle et archivez la précédente. Système de corbeille sécurisée (48h).
- **📋 Historique** : Suivi local de toutes les actions importantes effectuées dans l'application.

## 🛠️ Technologies Utilisées

- **Frontend** : HTML5, CSS3 (Vanilla), JavaScript (ES6 Modules).
- **Stockage & Chiffrement** : 
  - `IndexedDB` pour le stockage des vidéos et données.
  - `Web Crypto API` (AES-GCM) pour le chiffrement des données avec le code PIN utilisateur.
- **PWA** : Service Workers pour le mode hors-ligne et Manifest pour l'installation sur l'écran d'accueil.

## 🛡️ Confidentialité et Sécurité

La confidentialité est au cœur du projet :
- **Zéro Serveur** : Vos vidéos ne sont jamais téléchargées sur un serveur. Elles restent dans la base de données locale (`IndexedDB`) de votre navigateur.
- **Chiffrement par PIN** : Votre code PIN à 4 chiffres sert de clé de déchiffrement. Sans lui, les données sont illisibles.
- **Authentification locale** : L'accès à l'application est protégé par votre session locale.

## 🚀 Installation

### Sur Smartphone (Recommandé)
1. Ouvrez l'application dans votre navigateur (Safari sur iOS, Chrome sur Android).
2. Appuyez sur **"Installer l'application"** ou utilisez le menu de partage pour choisir **"Sur l'écran d'accueil"**.

### Développement Local
Pour lancer le projet localement :
1. Clonez le dépôt.
2. Servez les fichiers via un serveur HTTP local (ex: `npx serve .` ou l'extension "Live Server" de VS Code).
   > **Note** : Le protocole `https://` (ou `localhost`) est requis pour le fonctionnement des Service Workers et de l'appareil photo.

## 📁 Structure du Projet

```text
├── css/            # Feuilles de style (design system, composants)
├── js/             # Logique applicative (app.js, crypto.js, ui.js)
├── icons/          # Logos et icônes PWA
├── index.html      # Page de connexion / Accueil
├── dashboard.html  # Tableau de bord principal
├── script.html     # Éditeur de script
├── record.html     # Studio d'enregistrement (Téléprompteur)
├── tutoriel.html   # Guide d'utilisation
└── sw.js           # Service Worker (Gestion du cache / Offline)
```

## 📄 Licence

Ce projet est destiné à un usage personnel et médical dans le cadre du rétablissement en psychiatrie.
Voir [Psycom - Kit Mon GPS](https://www.psycom.org/agir/la-defense-des-droits/kit-mon-gps/) pour les ressources théoriques sur les DAP.
