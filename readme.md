# FOAD administration linux

LA **FOAD** du jour va consister en 2 projets :

## Premiere projet 
### Docker 

Aller sur la plateforme : [Play with Docker Classroom](https://training.play-with-docker.com/) et faire le parcours tutoriel : **Getting Started Walk-through for Developers > Stage 1: The Basics > Docker for Beginners - Linux** 

Dans la derniere partie du parcours créer un fichier **index.html** personnalisé avec votre contenu , dans votre environement (qui à base de la distribution linux alpine , que vous pouvez verifier enfaisant `cat /etc/os-release`) installer **nano** en faisant `apk add nano` (ou pour les aventuriers utiliser vim qui est déjà installé) ensuite bien mettre ce fichier dans l'image **docker** que vous allez créer et mettre l'image sur le **hub.docker.com** comme indiqué dans le tutoriel.
 
## Deuxiéme projet
### Serveur 

Installer un **serveur** avec les spécifications suivantes , libre à vous de choisir l'outil (**Vagrant**,**VirtualBox**) :

* Systéme d'exploitation: **Debian (12 ou 13)**
* CPU : **2** 
* RAM : **2Go**
* Disque dur : **20Go** 
* Ajouter un **utilisateur** nommé **foad** avec des droits **sudo** , permettre à l'utilisateur **foad** de ne pas entrer son mot de passe à chaque fois qu'il accede aux droits **administrateur**
* Installer les applications suivantes : **ufw,docker**

### Securisation du serveur
* Créer un **script** **bash** pour mettre à jour le systeme d'exploitation du **serveur** , le rendre **éxécutable** et le mettre dans `/usr/local/bin/`  
* Sécuriser votre **serveur** en générant des clefs **SSH**
* Ne pas permettre a **root** de se connecter a la machine
* Ajouter les **régles** nécéssaires pour le pare feu **ufw** pour sécuriser votre **serveur**
* Installer et lancer l'application à travers **docker** :
  * Récupérer l'**image** que vous **uploader** sur **hub.docker.com**
  * Créer un **container** avec votre **image** pour lancer votre application


## Les livrables

Voici les livrables que vous devez donner :

Créer un depot sur **github** ou autres plateformes d'hebergement git que vous nommerez **foad-admin-linux** , sur ce **dépôt** vous devrez  :

* Créer un **readme** pour :
  * expliquer la création de votre image **docker** et la création de **containeurs** avec votre image **docker** du **projet 1**
  * expliquer votre mise en place du serveur du **projet 2**
* Dans votre **dépôt** créer un dossier **media** ou vous mettrez les **captures d'ecrans** suivantes (vous en avez quelques examples dans ce dépôt) :
  * Capture d'ecran du terminale à droite dans derniere étape du **projet 1** quand vous faite votre push de votre image **docker** sur **hub.docker.com** que vous nommerez **fal-00.(png ou jpg)**
  * Votre machine dans **Virtualbox** que vous nommerez **fal-01.(png ou jpg)**
  * Dans la console de votre serveur du projet 2 taper **hostnamectl** et faire une capture d'ecran du résultat nommé **fal-02.(png ou jpg)** 
  * Donner une capture d'ecran de votre entrée pour la connexion à votre serveur dans le fichier **~/.ssh/config** nommé **fal-03.(png ou jpg)**  
  * Pour le project 2 faire une capture d'ecran de la commande `docker run --rm hello-world` nommé **fal-04.(png ou jpg)**  
* Mettre dans votre dépôt le fichier **sshd_config** de votre serveur en le nettoyant de toutes lignes commentées avec *#* pour ne laisser que les lignes nécéssaires

