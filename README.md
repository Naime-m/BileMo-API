#BileMo API

Septième projet dans le cadre de ma formation de développeur PHP Symfony chez OpenClassrooms

Pour installer le projet il faudra :

# 1 - CREATION DU FICHIER .ENV

Créer un fichier .env en se basant sur le fichier .env.example :

Ce fichier est strictement confidentiel et ne doit pas être partagé publiquement puisqu'il contiendra des données sensibles
tels que des mots de passe
Placez le fichier dans le même dossier que le fichier .env.example

# 2 - CONFIGURATION DU FICHIER .ENV

---------------------------------------
DATABASE_URL="mysql://test:@127.0.0.1:3306/mydatabase?serverVersion=5.7"
---------------------------------------

Après DATABASE_URL, il faudra indiquer l'adresse de votre base de données : 
https://symfony.com/doc/current/doctrine.html#configuring-the-database
Vous aurez les instructions à suivre selon votre base de données ici

# 3 - CREATION DE LA BASE DE DONNEES

Il faudra ensuite lancer la commande : php bin/console doctrine:database:create
Pour cela il faudra ouvrir votre invite de commande et être dans le dossier courant :
http://codeur-pro.fr/invite-de-commande-et-terminal/

# 4 - MISE A JOUR DE LA BASE DE DONNEES

Il faudra mettre la base de données à jour en utilisant à nouveau l'invite de commandes et lancer :
doctrine:schema:update 

Ceci mettra à jour la base de données

Si ça ne fonctionne pas, lancez cette commande : 

php bin/console doctrine:migrations:migrate

# 5 - LANCEMENT DU SERVEUR

Pour pouvoir lancer l'API, vous devrez démarrer un serveur local dans l'invite de commandes avec cette ligne :

php -S localhost:8000 -t public/


# 6 - ACCEDER A L'API

Il ne restera plus qu'à accéder à l'api à l'adresse suivante :

http://localhost:8000/api

