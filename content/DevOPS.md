+++
date = "2024-11-16T11:19:15+01:00"
draft = false
title = "DevOPS"
[cover]
    image = "/images/ArbreBlanc.jpeg"
    alt = ""
    caption = "*Le Gondor appelle à l'aide !*"
+++

---
# Résumé 

- [Ansible](#ansible)
- [Docker](#docker)
- [GITHUB sur le dépôt ➡️](https://github.com/NicolasW-7/AIS-DevOPS/tree/main/DevOPS)
- Crypto [**PKI**](/Procedures/PKI)
- [Rapport d'audit Linux et Windows et playbook Ansible lié sur le dépôt](https://github.com/NicolasW-7/AIS-DevOPS/tree/main/DevOPS/Audit)
---

# Ansible 

# ![ANSIBLE](https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white)

**Ansible est composé de trois concepts clés :**

- Inventaires : la liste des serveurs ou machines à gérer.
- Modules : des actions que l’on veut réaliser, comme installer un paquet, copier un fichier ou démarrer un service.
- Playbooks : des scripts qui orchestrent plusieurs modules pour accomplir une tâche complète.

*Ansible exécute des "instructions" appelées playbooks pour gérer ou configurer un ensemble de serveurs. Ces instructions sont écrites dans un langage clair (YAML), donc facile à lire, et elles sont structurées pour dire à Ansible quoi faire et sur quelles machines.*

## Les concepts principaux :

- Inventaire : L’inventaire est un fichier où l’on liste les machines cibles sur lesquelles Ansible va travailler. Chaque machine ou groupe de machines est associé à un nom (par exemple, web_servers pour tous les serveurs Web). L'inventaire par défaut se trouve dans /etc/ansible/hosts, mais vous pouvez créer un fichier d’inventaire personnalisé.

- Modules : Ce sont les “outils” qu’Ansible utilise pour exécuter des actions. Par exemple, un module d'installation de logiciel comme apt (pour les serveurs Ubuntu/Debian) installe des paquets, un module service démarre des services, etc. Ansible propose des centaines de modules pour gérer toutes sortes de tâches.

- Playbooks : Un playbook est un fichier YAML où l’on définit une série d'actions (ou tâches) pour configurer ou gérer les machines. C'est ici que l'on orchestre les modules pour réaliser des opérations précises.


# Comment installer ANSIBLE

*Ansible est inclus dans les dépôts officiels, donc vous pouvez l’installer directement :*

```bash
sudo apt update
sudo apt install -y ansible
```
Exemple simple de playbook :

```yaml
Copier le code
- name: Configurer les serveurs web
  hosts: web_servers
  become: yes

  tasks:
    - name: Installer nginx
      apt:
        name: nginx
        state: present
```

## Comment exécuter un playbook

**Pour exécuter un playbook, on utilise la commande suivante :**

```bash
Copier le code
ansible-playbook -i <inventory_file> <playbook_file.yml>
```
-i : Spécifie le fichier d'inventaire.
playbook_file.yml : C’est le fichier contenant les tâches à exécuter.

## Les avantages d’Ansible
- Simplicité : Pas besoin d'installer de logiciel sur les machines gérées. Il suffit d’avoir accès en SSH.
- Facilité de lecture et d'écriture : Les fichiers YAML sont simples à lire et à comprendre, même pour les débutants.
- Automatisation sans agent : Contrairement à d'autres outils, Ansible ne nécessite aucun agent spécial sur les machines cibles, ce qui réduit la complexité de gestion.

## Exemple de playbook ansible 

[Playbook Ansible correction du rapport d'audit Linux](/procedures/PlaybookAnsible)

[TOP⬆️](#résumé)

![Illustration](/images/Rohan.jpeg)

# Docker

# ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

Docker est une plateforme qui permet de créer, déployer et exécuter des applications à l’intérieur de containers. Un container est une unité standardisée de logiciel qui emballe le code et toutes ses dépendances, de sorte que l’application puisse s'exécuter de manière rapide et fiable d'un environnement à un autre.

![Docker](/images/Docker.jpg)

## Fonctionnement de Docker :

- Images Docker : Une image est un modèle statique contenant tout ce dont une application a besoin pour fonctionner (code, bibliothèques, dépendances). Les images Docker sont créées à partir d'un fichier de configuration appelé Dockerfile, qui définit la structure de l'image.

- Containers Docker : Un container est une instance exécutable d’une image. Lorsqu'une image est lancée, Docker crée un container qui isole l’application de l’environnement sous-jacent tout en permettant à celle-ci de fonctionner normalement. Plusieurs containers peuvent être exécutés à partir de la même image.

- Docker Daemon : C’est le processus principal qui gère les containers Docker. Il écoute les requêtes Docker et exécute les instructions pour créer, démarrer, arrêter ou supprimer des containers.

- Docker CLI : La ligne de commande Docker (CLI) permet à l’utilisateur de communiquer avec le daemon Docker pour exécuter des commandes comme docker run, docker build, docker ps, etc.

## Commandes principales :

- docker build : Crée une image à partir d'un Dockerfile.
- docker run : Lance un container à partir d’une image.
- docker ps : Affiche les containers en cours d’exécution.
- docker stop : Arrête un container.
- docker exec : Exécute des commandes dans un container en cours d'exécution.

# Docker Compose

![Docker](/images/DockerCompose.png)

Docker Compose est un outil qui permet de définir et gérer des applications multi-containers. Il utilise un fichier YAML (docker-compose.yml) pour décrire les services, réseaux et volumes nécessaires à l'application.

## Fonctionnement de Docker Compose :

- Fichier docker-compose.yml : Il contient la définition des services (containers), volumes et réseaux nécessaires pour faire fonctionner une application. Chaque service peut être une image Docker différente, avec des paramètres spécifiques comme les ports, volumes partagés, variables d’environnement, etc.

- Déploiement multi-containers : Avec Docker Compose, on peut définir plusieurs services qui s’exécutent ensemble. Par exemple, une application web peut avoir un service pour le serveur web (comme Nginx), un autre pour la base de données (comme MySQL), etc. Compose gère les interactions entre ces services.

## Commandes principales de Docker Compose :

- docker-compose up : Démarre les containers définis dans le fichier docker-compose.yml.
- docker-compose down : Arrête et supprime les containers, réseaux et volumes.
- docker-compose build : Reconstruit les images à partir des configurations.
- docker-compose logs : Affiche les logs des services.
  
Exemple de fichier docker-compose.yml :

https://github.com/NicolasW-7/AIS-DevOPS/blob/main/DevOPS/Docker/docker-compose.yml

[Sur le site dans Procédures](/Procedures/dockercompose)


## Résumé des différences :
- Docker : Permet de gérer des containers individuels.
- Docker Compose : Permet de gérer plusieurs containers en tant qu'application, avec un fichier de configuration unique.

[TOP⬆️](#résumé)

![Illustration](/images/Mordor.jpeg)