# Install Docker on Ubuntu
>for more installation details see [Docker doc ubuntu](https://docs.docker.com/engine/install/ubuntu/#set-up-the-repository) and [Docker Get started](https://www.docker.com/get-started/)

> Verify that the Docker Engine installation is successful by running the hello-world image.
```bash
sudo docker run hello-world
```

| use |command |
|---|---|
| Afficher les conteneurs en cours d'exécution  |  sudo docker ps |
| Afficher tous les conteneurs, y compris ceux qui ne sont pas en cours d'exécution.|  sudo docker ps -as |
|  création image | docker build -t nomimage:version .  |
|  lister mes images | sudo docker image ls  |
|  lister history des commandes dans mon images | sudo docker history nomimage:version  |
|permet de créer et de démarrer un nouveau conteneur Docker en utilisant une image spécifique et de lui donner un nom personnalisé.|sudo docker run -tid --name test nomimage:version|
|se connecter à notre conteneur|sudo docker exec -ti test sh|
|stoperun conteneur |sudo docker stop 3a73b3d8cc15 (container ID))|
|loger dockerhub|sudo docker log|
|tager l'image avant de pousser|sudo docker tag cpluscplus-ci-copy:v0 samibenelhajsalah/image-docker-hub|
| push vers dockerhub| sudo docker push samibenelhajsalah/image-docker-hub|
|supprimer le conteneur (**absolument avant de supprimer l'image**)|sudo docker rm -f test|
|supprimer l'image |sudo docker rmi nomimage:version|

> **_NOTE:_  :pencil2:**  Remaks:

>-tid: Ces options sont utilisées ensemble pour exécuter le conteneur en mode détaché (en arrière-plan) et fournir un accès interactif au terminal du conteneur. 

>L'option -t associe le terminal à l'entrée standard du conteneur, tandis que l'option -i permet  