# 📚 Mon Vieux Grimoire

Application web de notation et de référencement de livres.
Projet réalisé dans le cadre de la formation **OpenClassrooms - Développeur Web**.

## 🛠️ Stack technique

- **Node.js** / **Express** — serveur et API REST
- **MongoDB** / **Mongoose** — base de données
- **JWT** — authentification sécurisée
- **Multer** / **Sharp** — upload et optimisation d'images
- **Bcrypt** — hashage des mots de passe

## ✨ Fonctionnalités

- Création de compte et connexion utilisateur
- Ajouter, modifier, supprimer un livre
- Upload de couverture de livre
- Système de notation (1 à 5 étoiles)
- Calcul de la note moyenne par livre

 ## 🔗 API Endpoints

 API REST sécurisée permettant la gestion de livres et des utilisateurs.

- `GET /api/books/:id` → récupérer un livre
- `PUT /api/books/:id` → modifier un livre
- `DELETE /api/books/:id` → supprimer un livre
- `POST /api/books/:id/rating` → noter un livre
- `GET /api/books/bestrating` → livres les mieux notés

## 🚀 Installation

### Prérequis
- Node.js installé
- MongoDB (local ou Atlas)

### Lancer le projet

```bash
# Cloner le repo
git clone https://github.com/Elkes-dev/Mon-Vieux-Grimoire.git

# Installer les dépendances
cd Mon-Vieux-Grimoire
npm install

# Lancer le serveur
npm start
```

### Variables d'environnement
Crée un fichier `.env` à la racine :
```
MONGODB_URI=chaine_de_connexion
JWT_SECRET=secret
SALT_ROUNDS=nombre_hachage
```
## 🔐 Sécurité

- Authentification avec JWT
- Mots de passe hashés avec bcrypt
- Validation des données côté serveur

## 🖼️ Optimisation des images

Les images uploadées sont compressées et redimensionnées automatiquement avec Sharp afin d’optimiser les performances.

## 📁 Structure du projet

```
├── controllers/ # Logique métier
├── middlewares/ # Auth, upload
├── models/ # Schémas Mongoose
├── routes/ # Routes API
├── images/ # Images uploadées
├── app.js
└── server.js
```
```
