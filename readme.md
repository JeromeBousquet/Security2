DEPLOY SECURE APPS (part two)
===

![center](/fb.png)

<h3>Lundi</h3>

**Retour alternance**

**Veille sur les outils de dev du navigateur**

**Monday Algo live coding**

*Ecrire un prog java qui doit, pour un tableau contenant X nombres donné, retourner la somme des 2 plus grands nombres présent dans ce tableau.
Exemple: avec le tableau [78, 6, -250, 2, 12, 9], le résultat sera 90*

**De retour sur l'application de gestion des taches : MISE EN OEUVRE DE LA PARTIE FRONT**

*Même si la partie front n'est pas très importante ici, il est recommandé de réaliser la maquette de l'application avant de commencer*

*L'application dipose donc d'un menu ou 2 boutons/actions :*
*- ouverture de la page d'authentification (page d'acceuil)*
*- liste des taches accessible au niveau du back une fois connecté (token en local storage)*

*Par défaut, l'appli affiche le composant d'authentification avec 2 possibilitées :*
*- Un bouton login après saisie id + pwd*
*- Un bouton pour enregistrer un nouvel utilisateur*

60.1 Créer une application Angular avec votre Ide préféré
60.2 Installer Bootstrap3 dans le projet
60.3 Installer Jwt dans le projet

60.4 Ajouter un composant login pour l'authentification
60.5 Ajouter un composant task pour afficher la liste des taches
60.6 Ajouter un composant nouvelle tache pour rajouter une tache (uniquement pour les administrateurs)
60.7 Ajouter un composant pour enregistrer un nouvel utilisateur

60.8 Ajouter les routes associées à ces composants
60.9 Sur la page d'accueil, ajouter 2 boutons qui ouvrent les composants login et tasks

<h3>Mardi</h3>

**Veille sur le protocole Http**

61.1 Réaliser un formulaire d'authentification sur le composant login
61.2 Ajouter un service dédié à l'authentification servant à vérifier côté back si un user a des droits

61.3 Côté back, autoriser les requetes provenant d'autre domaine
61.4 Côté back, trouver un moyen d'authoriser l'accès au token envoyé sur le front, vérifier !

61.5 Côté front, une fois autorisé, stocker le token dans le local storage puis afficher la liste des taches
61.6 Trouver une solution en cas de token expiré ou malveillant

<h3>Mercredi</h3>

**Veille sur comment tester les failles de sécurité d'une api/appli**

62.1 Ajouter un bouton dans la liste des taches permettant uniquement aux administrateurs d'ajouter des nouvelles taches 
-> Attention ici, le bouton ne doit pas s'afficher pour les utilisateurs
-> Gérer aussi le cas ou un utilisateur tente d'accéder à l'url d'une nouvelle tache sans être admin
-> Tester tous les cas de figures pour empêcher toutes les utilisations malveillantes de l'appli
-> Veiller à ce que l'enchainement des fenêtres soit logique et cohérent, se connecter revient à avoir accès aux taches et inversement
-> Trouver toujours des moyens pour limiter les accès au serveur, le faire que lorsque c'est indispensable

62.2 S'agissant de l'ajout d'une tache, faites en sorte d'imposer une saisie et ne sauvegarder que dans ce cas

**Retour sur Heroku**

63.1 Il s'agit ici de mettre votre back sur heroku puis de tester avec votre appli front
63.2 Effectuer tous les tests de sécurité de votre api
63.3 Challenger les autres développeurs en les invitant à tenter de hacker votre api
63.4 Mettez en ligne votre appli front et refaite des tests de sécurité

64.1 Ajouter les fonctionnalités liées à un nouvel utilisateur puis tester le tout

**Bonus : refaite de même avec une autre appli(Banquaire, E-commerce, Réservation hotels)**

<h3>Jeudi</h3>

**Veille OpenId Connect & Auth0**

*Reprenez l'api de gestion des entreprises puis utiliser Keyclock pour gérer les accès sécurisés*
65.1 Nous travaillons en local aussi, basculer le sgbd vers H2
65.2 Installer Keyclock puis lancer le serveur
65.3 Ajouter un Realm "simplon"
65.4 Ajouter une dépendances keyclock(dernière version stable) + spring security
65.5 Ajouter une classe de configuration spring pour la gestion de la sécurité basée sur keycloak
65.6 Enfin, ne permettez l'accès à votre api qu'aux utilisateurs authentifiés/autorisés
65.7 Configurer le fichier application.properties en conséquence
65.8 Dans la console de keycloak, déclarer l'application (add-client...)
65.9 Ajouter un utilisateur avec password puis TESTER LE TOUT
*Vous pouvez continuer à bidouiller l'outil qui permet la gestion de nombreuses fonctionnalités*
-> mot de pass oublié, se rappeler de moi, nouvel utilisateur...

![center](/keycloak.png)

**Bonus : refaite de même avec une autre appli(Banquaire, E-commerce, Réservation hotels)**

<h3>Vendredi</h3>

**Veille sur l'adaptabilité en entreprise/équipe**

Terminer tous les travaux de la semaine et les envoyer sur github puis transferer à vos tuteurs(rices) et formateur avec les comptes rendus

**Dossier professionnel**

**Dossier projet**


RESSOURCES
===

[tuto angular app](https://www.youtube.com/watch?v=nx9gREsP4j8)

[Authentication with JWT Tutorial](https://www.techiediaries.com/angular-jwt/)
[Decode JSON Web Tokens (JWT) in Angular — onthecode](https://onthecode.co.uk/decode-json-web-tokens-jwt-angular/)

[Angular Security - Authentication With JWT: The Complete Guide](https://blog.angular-university.io/angular-jwt-authentication/)

[Getting Started Guide Keyclock](https://www.keycloak.org/docs/latest/getting_started/index.html)
[Tuto Spring boot app with keycloak](https://www.youtube.com/watch?v=0cziL__0-K8)
