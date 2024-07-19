# Dockerfile pour l'API REST (BACKEND).

# Image node choisie avec la version.

FROM node:latest

# On se met dans l'emplacement où se trouve nos données de service.

WORKDIR /usr/src/app

# On copie le fichier package.json dans l'emplacement actuel.

COPY package.json ./package.json

# Lancement du service npm (qui est une dépendance dans l'image node js).

RUN npm install --save cors apollo-server-express express graphql@14 reflect-metadata type-graphql@0 apollo-datasource-rest soap jsonwebtoken --legacy-peer-deps

# Copie du répertoire courant dans le répertoire actuel.

COPY . .

# Exposition du port 8080 de notre service API REST.

EXPOSE 8080

# Exécution dans le CMD de notre conteneur du service npm, que l'on démarre.

CMD [ "npm", "start" ]