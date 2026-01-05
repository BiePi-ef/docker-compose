# Projet Docker #2

## Introduction
Ce projet consistait à build 2 microservices Java dans 1 docker compose, et à vérifier que l'un puisse communiquer avec le second.
Comme dans mon premier projet, les Dockerfile des 2 microservices buildent les projets Java avant la création de l'image (dans les fichiers Dockerfile)

## Run le projet :

> docker compose up
ou 
> docker compose up -d

*resultat du build / run*
![screenshot docker composer up 1](images/image.png)
![screenshot docker composer up 2](images/image2.png)
![screenshot docker composer up 3](images/image3.png)

Pour arreter les containers :

> docker compose down
(ou ctrl + c si le container était lancé en mode detached (-d))

### Test :
On peut tester la methode "bonjour" de notre microserice 'RentaService' pour vérifier qu'il appelle bien le microservice customer :

> curl -s http://localhost:8080/customer/Jean%20Dupont

*l'appel renvoit :*
![test de l'url ](images/image4.png)

## Bonus : BDD avec volumes
// tdo