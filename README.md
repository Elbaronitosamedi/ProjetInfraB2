# Projet Infra B2

## Prérequis

* Une marchine pouvant servir de serveur ou un vps (sous linux de préférence)
* Avoir Docker d'installé avec un user dédié (si besoin voici un lien vers la doc officielle pour vous aider : https://docs.docker.com/engine/install/ )



## Installation et Set up

* Clonnez le repository :
    ```git clone https://github.com/Elbaronitosamedi/ProjetInfraB2.git```

* Build les contenurs :
    - dans /App :
        ```docker build -t app .```
    - dans /nginx : 
        ```docker build -t reversenginx .```

* Lancer le docker-compose :
    ```docker-compose up --build -d```

* Pensez à ouvrir le ports 80 de la machine :
    exemples à l'aide de ``firewalld`` : 
    * `sudo firewall-cmd --add-port=80/tcp --permanent`
    * `sudo firewall-cmd --reload`


* Configurez la redirection de port si vous héberger chez vous (ne pas oublier le dyndns)

* Configurer votre nom de domaine pour qu'il pointe soit vers voter VPS soit votre box

## Test

Si tout va bien vous pourrez accéder à votre site depuis n'importe quel navigateur.

Attention quand même si c'est le premier lancement du site il peut y avoir un délai avant que votre site soit correctement indexé.cd