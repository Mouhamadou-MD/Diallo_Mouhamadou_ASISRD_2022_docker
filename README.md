# Bienvenue sur le référentiel


#Explications des services
L'architecture est composée de 3 services qui sont APP, API RES et MongoDB. 

- L'APP qui tourne sur reactJS et nodeJS, va afficher une page web afin de récolter les données.
> Ce service se trouve du coté frontend.
	
- L'API RES qui tourne sur nodeJS va communiquer les donnés à la base de données MongoDB.
> Ce service se trouve du coté backend.

- MongoDB qui tourne en noSQL est une base de donnée qui va enregistrer les données au sein de sa base.
 > Ce service se trouve du coté backend.

## Explication de l'architecture 
L'architecture est séparée en deux. D'un côté il y a le Frontend où est situé le services APP et de l'autre côtés il y a le Backend où sont situés les services MongoDB et API RES.
L'utilisateur n'est pas au courant de ce qui se passe du côté Backend.

L' API est l'APP ont tous d'eux un Dockerfile tandis que MongoDB à une image officielle. 

L'architecture comporte: 
- 3 images
- 6 ports d'écoutes
- 3 containers 
- 1 docker-compose.yml

#Les Commandes 

Construire une nouvelle image
docker image build -t frontend:1.0 .			<= images frontend
docker image build -t backend:2.0 .  			<= images backend

Vérifier les images 
docker images

Récuperer une image sur le repository
docker pull mongo 					<= image mongo 

Instancier un nouveau conteneur
docker container run -p 4430:9327 frontend:1.0  	<= container frontend
docker container run -p 4431:9328 backend:2.0  		<= container backend
docker container run -p 4432:9329 mongo:3.0  		<= container mongo

Vérifier les conteneurs en route (qui sont up)
docker ps

Vérifier  les  conteneurs  qui ne  sont  pas  lancés
docker ps -a

Créé et demarré les services du fichier 
docker-compose up

Stoper les services du fichier 
docker-compose stop

Activer les services du fichier 
docker-compose start

Arrêter et supprimer les services du fichier
docker-compose down 

#Auteurs Mouhamadou Diallo
   