# Étape 1 : Utiliser une image de base Node.js légère
FROM node:lts-alpine

# Étape 2 : Définir le répertoire de travail
WORKDIR /usr/src/app

# Étape 3 : Copier les fichiers de gestion des dépendances
COPY package*.json ./

# Étape 4 : Installer les dépendances
RUN npm install

# Étape 5 : Copier le reste du code source
COPY . .

# Étape 6 : Construire l'application React pour la production
RUN npm run build

# Étape 7 : Installer un serveur HTTP léger pour servir les fichiers statiques
RUN npm install -g serve

# Étape 8 : Exposer le port 3000
EXPOSE 3000

# Étape 9 : Commande pour démarrer le serveur et servir les fichiers du dossier 'build'
CMD [ "serve", "-s", "build", "-l", "3000" ]
