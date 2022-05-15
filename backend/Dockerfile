# Image de base
FROM node:8.11-alpine

#Copie de la liste des dependances 
COPY package.json /app/package.json

#Installation des dependances
RUN cd /app && npm install 

#Copie du code app
COPY . /app

#Répertoire de travail de l'app
WORKDIR /app

#Port d'écoute
EXPOSE 4430

#Lancement
CMD ["npm", "start"]
