# Node
Cours Openclassroom sur Node / Express / MongoDB

### Informations générales 
Etant en pleine formation Full Stack, je suis en parallèle le cours "Passez au Full Stack avec Node.js, Express et MongoDB" d'openclassrooms. 

### Installation 
- Pour installer cette application, j'ai cloné le code de l'application front-end dans un sous-répertoire appelé 'frontend' comme indiqué dans le cours
-> Commande git clone https://github.com/OpenClassrooms-Student-Center/go-fullstack-v3-fr.git frontend

- Installation de toute les dépendances et lancement du serveur de développement. 
-> cd frontend
npm install
npm run start

- Création d'un dossier "backend" puis commande 'npm init' pour initialiser le projet. 
- Création d'un fichier server.js dans le dossier "backend"
- Création d'un server node dans le fichier server.js avec le code suivant : 

const http = require('http');
const server = http.createServer((req, res) => {
    res.end('Voilà la réponse du serveur !');
});
server.listen(process.env.PORT || 5500);

- Installation de nodemon avec la commande : npm install -g nodemon
- Installation d'express avec la commande : npm install express
- Création d'un fichier app.js dans le quel est placé l'application express : 

const express = require('express');

const app = express();

module.exports = app;

- Modification du fichier server.js : 
const http = require('http');
const app = require('./app');

app.set('port', process.env.PORT || 3000);
const server = http.createServer(app);

server.listen(process.env.PORT || 3000);

- 

