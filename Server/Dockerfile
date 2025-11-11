# Étape 1 : Utiliser une image de base Node.js légère
FROM node:lts-alpine

# Étape 2 : Définir le répertoire de travail dans le conteneur
WORKDIR /usr/src/app

# Étape 3 : Copier les fichiers de gestion des dépendances
COPY package*.json ./

# Étape 4 : Installer les dépendances
RUN npm install

# Étape 5 : Copier le reste du code source de l'application
COPY . .

# Étape 6 : Exposer le port sur lequel l'application va écouter
EXPOSE 9000

# Étape 7 : Définir la commande pour démarrer l'application
CMD [ "npm", "start" ]
