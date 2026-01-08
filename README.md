# GENZ212 France - Mémoire vivante & Archives

Site web d'archives participatives pour la préservation de la mémoire collective d'un mouvement social.

## 📋 Description

GENZ212 France est une plateforme complète permettant à chaque utilisateur de :
- Créer un compte sécurisé (email + mot de passe)
- Publier des témoignages et récits personnels
- Partager des photos, vidéos, fichiers audio
- Commenter et réagir aux publications
- Rechercher des contenus par mots-clés, dates, catégories
- Explorer une timeline chronologique des événements
- Visualiser une carte interactive des témoignages
- Naviguer par thématiques (police, manifestations, solidarité, etc.)

## 🚀 Technologies utilisées

### Backend
- **Node.js** + **Express** : Serveur web
- **SQLite** : Base de données (facile à déployer)
- **JWT** : Authentification sécurisée
- **Multer** : Upload de fichiers
- **bcryptjs** : Cryptage des mots de passe

### Frontend
- **HTML5 / CSS3** : Structure et design
- **JavaScript Vanilla** : Interactivité
- **Leaflet** : Carte interactive
- Design **responsive** et **mobile-first**

## 📦 Installation

### Prérequis
- Node.js (version 14 ou supérieure)
- npm (inclus avec Node.js)

### Étapes d'installation

1. **Cloner ou télécharger le projet**
   ```bash
   cd GENZ212FRA
   ```

2. **Installer les dépendances**
   ```bash
   npm install
   ```

3. **Créer le fichier de configuration**
   ```bash
   cp .env.example .env
   ```

4. **Modifier le fichier .env**
   Ouvrez `.env` et modifiez :
   ```
   PORT=3000
   JWT_SECRET=votre_secret_ultra_securise_a_changer
   NODE_ENV=production
   ```

5. **Démarrer le serveur**
   ```bash
   npm start
   ```

6. **Accéder au site**
   Ouvrez votre navigateur : `http://localhost:3000`

## 🎨 Structure du projet

```
GENZ212FRA/
├── backend/
│   ├── server.js              # Serveur principal
│   ├── config/
│   │   └── db.js              # Configuration base de données
│   ├── routes/
│   │   ├── auth.js            # Routes authentification
│   │   ├── posts.js           # Routes publications
│   │   ├── comments.js        # Routes commentaires
│   │   └── users.js           # Routes utilisateurs
│   ├── middleware/
│   │   └── auth.js            # Middleware JWT
│   └── uploads/               # Fichiers uploadés
├── frontend/
│   ├── index.html             # Page d'accueil
│   ├── login.html             # Connexion
│   ├── register.html          # Inscription
│   ├── feed.html              # Fil des publications
│   ├── post.html              # Créer une publication
│   ├── profile.html           # Profil utilisateur
│   ├── memoire.html           # Mémoire collective
│   ├── faq.html               # Questions fréquentes
│   ├── contact.html           # Contact
│   ├── css/
│   │   └── style.css          # Styles principaux
│   └── js/
│       └── app.js             # Fonctions JavaScript
├── package.json
├── .env.example
└── README.md
```

## 📖 Utilisation

### Créer un compte
1. Cliquez sur "S'inscrire"
2. Remplissez le formulaire (nom d'utilisateur, email, mot de passe)
3. Vous êtes automatiquement connecté

### Publier un témoignage
1. Connectez-vous
2. Cliquez sur "Publier"
3. Remplissez le formulaire
4. Cliquez sur "Publier"

### Interagir avec les publications
- **Réagir** : Cliquez sur ❤️ pour soutenir
- **Commenter** : Cliquez sur 💬 pour commenter
- **Signaler** : Cliquez sur ⚠️ pour signaler un contenu inapproprié

## 🔒 Sécurité

- Les mots de passe sont **cryptés** avec bcrypt
- Authentification par **JWT** (tokens sécurisés)
- Protection contre les injections SQL
- Validation des fichiers uploadés
- Système de **signalement** des contenus inappropriés

## 🌐 Déploiement

### Déploiement local
```bash
npm start
```

### Déploiement sur un serveur
Utilisez PM2 pour maintenir le serveur actif :
```bash
npm install -g pm2
pm2 start backend/server.js --name genz212
pm2 save
pm2 startup
```

## 📊 Base de données

Le projet utilise SQLite par défaut (fichier `backend/database.db`).

### Sauvegarder la base de données
```bash
cp backend/database.db backup-$(date +%Y%m%d).db
```

## ⚠️ Important

- **Changez le JWT_SECRET** dans `.env` avant de déployer en production
- **Sauvegardez régulièrement** la base de données
- **Respectez la vie privée** des utilisateurs
- **Modérez les contenus** inappropriés

---

**GENZ212 France** - Préserver la mémoire, construire l'avenir 🇫🇷
