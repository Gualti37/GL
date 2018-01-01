Nom & Prénom des participants au projet : Gualtiero Lugato
● Compte et accès : cd dans le repertoire du projet, ensuite:
sudo php bin/console server:run 
https://127.0.0.1:8000
https://github.com/Gualti37/GL pour la version en SqLite sur le git.
https://gualtiero-lugato-blog.herokuapp.com/ pour la version en ligne


● Commentaires : 

La version en ligne du projet disponible à l'adresse https://gualtiero-lugato-blog.herokuapp.com/
fonctionne bien niveau base de données.
Malheureusement il y a un problème sur le site deployé sur Heroku : le CSS du /login et /register ne fonctionne pas
ligne alors que en local tout marche très bien.
Dejà la différence entre ces templates et ces du reste de l'application c'est qu'ils sont des
templates dans app/Resources/FosUserBundle qui font le override des templates du FosUserBundle installé dans vendor/friendsofsymfony. 
Je ne m'explique pas cette différence entre ligne-local et à ce qu'il parait je suis le seul à avoir ce problème,
alors que j'ai la même structure des fichiers dans avec les mêmes heritages que d'autres copains de ma classe selon ce
qui est expliqué dans les plusieurs tutoriels en ligne sur ce sujet. J'ai même pris en bloc le FosUserBundle d'un copain pour tester et il y a toujours le même problème.

J'ai décidé donc de laisser une version en ligne et d'envoyer une autre version en SqlLite.

Droits :
- Chaque visiteur a le droit de voir les posts présents dans le blog.
- En cliquant sur le titre du post on a accés au contenu du post.
- Suppression/modification d'uun post existant : le droit de modifier/supprimer un
post est reservé à l'utilisateur qui est au même temps auteur de ce post.
- Autrement une exception est levée 

Inscription : 
- Le blog donne la possibilité à plusieurs auteurs de s'inscrire à la plateforme
- Une fois l'inscription effectuée, l'auteur peut acceder grace au login
- A cause des problèmes niveau templates dans la version en ligne il n y a plus le lien vers register qu'on peut avoir avec https://127.0.0.1:8000/register


Choix techniques :
- Usage de FosUserBundle pour l'inscription
- Deux controleurs : BlogBundle & CrudController
- Gestion des exceptions (alert)

2 utilisateurs sont déjà inscrits dans la base postgres online /SqLite en local :
username: user1 
password : dede1

username: user2
password : dede2

