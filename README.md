
# [](#installation-du-projet)Installation du projet 

Les technos :

- Docker (conteneur)

- Nginx (serveur web)

- Postgresql (base de donnée)

- Symfony avec API platform (API rest)
    - ApiPlatformBundle
    - DoctrineBundle
    - MakerBundle

Nginx tourne sur le port 80 de la machine physique et postgresql sur le port 5432 (celui par défaut), merci de laisser ces ports disponibles pour pour pouvoir travailler sur le projet

  
### Prérequis :

Docker :

[https://docs.docker.com/install/linux/docker-ce/ubuntu/](https://docs.docker.com/install/linux/docker-ce/ubuntu/)


Il vous faudra aussi docker compose pour gérer les différents containers :


[https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/)


## Set up de docker
```bash
# A exécuter à la racine du projet
sudo docker-compose up -d
```

```bash
# Installation des dépendances pour symfony
sudo docker-compose exec php composer install -d /php
```

## Création de la base de donnée

```bash
# A exécuter à la racine du projet
# Création de la base de donnée grâce à Doctrine
sudo docker-compose exec php /php/bin/console doctrine:database:create
```