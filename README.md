# 🌐 Backend API Utilisateur avec Node.js & Express

Ce projet est une API REST minimale construite avec **Node.js** et **Express.js**. Elle permet de gérer une liste d'utilisateurs avec des opérations CRUD (Créer, Lire, Mettre à jour, Supprimer).

---

## 🚀 Objectif

Découvrir Node.js et le framework Express en développant un backend simple.

---

## 📁 Structure du projet

```
backend-api/
│
├── index.js             # Fichier principal du serveur Express
├── package.json         # Informations du projet + dépendances
├── package-lock.json    # Dépendances exactes installées
└── node_modules/        # Dossier généré automatiquement avec les modules Node
```

---

## ✅ Fonctionnalités

- `GET /` → Message de bienvenue
- `GET /users` → Récupérer tous les utilisateurs
- `GET /users/:id` → Récupérer un utilisateur par ID
- `POST /users` → Ajouter un nouvel utilisateur
- `PUT /users/:id` → Modifier un utilisateur existant
- `DELETE /users/:id` → Supprimer un utilisateur

---

## ⚙️ Installation et exécution

### 1. Cloner le projet ou créer un dossier :

```bash
cd chemin/vers/ton/dossier
mkdir backend-api
cd backend-api
```

### 2. Initialiser un projet Node.js

```bash
npm init -y
```

### 3. Installer Express.js

```bash
npm install express
```

### 4. Ajouter le fichier `index.js`

Crée un fichier `index.js` et colle-y le code de l'API Express.

### 5. Démarrer le serveur

```bash
node index.js
```

📌 Le serveur sera accessible sur : [http://localhost:3000](http://localhost:3000)

---

## 🛑 Arrêter le serveur sur PowerShell (Windows)

Pour arrêter un serveur qui utilise un port spécifique comme 3000 :

### 1. Trouver le PID du processus :

```powershell
netstat -aon | findstr :3000
```

→ Note le **PID** affiché à la fin (ex: `46304`)

### 2. Terminer le processus :

```powershell
taskkill /PID 46304 /F
```

Remplace `46304` par le PID trouvé à l’étape précédente.

---

## 🔍 Exemple de requêtes

### GET tous les utilisateurs

```bash
curl http://localhost:3000/users
```

### POST un utilisateur

```bash
curl -X POST http://localhost:3000/users -H "Content-Type: application/json" -d "{\"name\":\"Charlie\", \"email\":\"charlie@example.com\"}"
```

---

## 📌 Remarques

- Les données sont **stockées en mémoire** (tableau `users`) → elles seront réinitialisées à chaque redémarrage.
- Ce backend est **idéal pour apprendre** les bases d’une API REST avec Node.js.

---

## 🧑‍💻 Auteur

Zgarni Rawen – Projet d’apprentissage Express.js

---

## 📄 Licence

Ce projet est libre d’utilisation à des fins pédagogiques.
