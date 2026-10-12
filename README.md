# GuestBook docker-compose

## Conteneuriser l'application guestbook
L'objecif est d'apprendre à réaliser un Dockerfile pour réaliser une image d'un conteneur et un docker-compose pour automatiser le l'execution du conteneur. 

### Problème rencontré et pourquoi il est survenu
Lors de la création de mon Dockerfile, j'avais mis une version de go inférieur à ce que j'avais donc ca ne marchait pas. Il y a également lorsque j'ai voulu lancer l'image 0.2.0.

### Solution appliquée et pourquoi cette solution fonctionne
Pour le problème de go c'est du au fait que go exigeait la version la plus moderne.
Aussi la partie RUN CGO_ENABLED=0 dans le Dockerfile, je ne l'avais pas mis mais il est important car sinon l'image scratch reste vide sans l'initialisation de cette variable.

### Ce que j'ai appris
J'ai appris le processus de création d'image docker.
Puis, une fois que ca fonctionne, on réalise un Docker-compose.yaml pour automatisé le processus de build et l'ouverture des ports.

---

## Ajouter une base de données à votre service
Le but est d'ajouter une BDD Redis à l'application.

### Problème rencontré et pourquoi il est survenu
Je ne savais pas comment dire à au service Guestbook comment acceder à Redis

### Solution appliquée et pourquoi cette solution fonctionne
Ajouter une variable d'environnement qui donne le nom du service de BDD Redis

### Ce que j'ai appris
Comment améliorer le docker-compose.yaml pour générer à la fois un service applicatif et le faire communiquer avec une BDD.

---

## Ajouter de la persistance et du hot-reloading au guestbook
Enregistrer les données dans un volume persistant et automatiser le build.

### Problème rencontré et pourquoi il est survenu
J'essaie de faire fonctionner le dockerfile avec plusieurs images.

### Solution appliquée et pourquoi cette solution fonctionne
J'ai retiré l'ancienne image from scratch.

### Ce que j'ai appris
J'ai appris le concept de Hot-Reloading et comment Air et le volume du service Guestbook fonctionne pour faire marcher le Hot-Reloading.

---

## Créer des stacks avec du hot-reloading


### Problème rencontré et pourquoi il est survenu


### Solution appliquée et pourquoi cette solution fonctionne


### Ce que j'ai appris
