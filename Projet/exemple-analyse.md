# Exemple d'analyse fonctionnelle

## Préambule

Bonjour à tous, voici un exemple sommaire d'une analyse rapidement effectuée pour une application permettant de créer, éditer, supprimer, stocker des TO DO List

## Landing Page = Log In page

A l'entrée de 

La page de connexion doit également permettre l'enregistrement.

### Connexion

Un bouton principal "CONNECT" ouvre une modale permettant la connexion de l'utilisateur via son identifiant et son mot de passe.
Cette modale comporte donc un formulaire, deux input permettant la saisie des identifiants. 
Ces inputs doivent être protégé contre les injections SQL basiques, le format e-mail doit être privilégier.
Le bouton connexion doit renvoyer les données du formulaire vers le serveur d'authentification.

Gestion de la connexion:

- Si l'utilisateur rentre un mauvais identifiant, spécifier "Identifiant ou mot de passe incorrect" -> rester sur la page de connexion
- Si l'utilisateur rentre ses identifiants correctement: rediriger vers sa page d'acceuil comportant ses To Do List

### Enregistrement

Le lien vers l'enregistrement ouvre également une modal mais cette fois permettant l'enregistrement de l'utilisateur. Ce formulaire doit comporter:

- Un champs nom d'utilisateur
- Un champs adresse e-mail
- Un champs mot de passe
- Un bouton "Sign In" permettant l'enregistrement des données dans la base de donnée

Gestion de l'enregistrement:

- Chaque utilisateur doit posséder un ID unique
- Chaque utilisateur doit voir son mot de passe crypté


## Navigation

Une fois connecté l'utilisateur a à sa disposition une barre de navigation. Celle ci comportant:
- Un lien retour vers la page d'index ainsi qu'un lien vers la page de settings permettant de modifier ses informations utilisateur 
- Un bouton de déconnexion.
Une fois l'utilisateur déconnecté il est redirigé vers la page de connexion.

## Index

L'index, ou page d'accueil, n'est accessible qu'aux membres enregistrés.
Il doit comporter:
- Un bouton pour ajouter une liste: ouvre une modale munie d'un formulaire
- La barre de navigation
- L'ensemble des listes sous forme de vignette: doit comporter le titre et les trois premières tâches
- Un bouton pour supprimer une liste
- Un bouton pour éditer une liste: ouvre une modale permettant d'éditer le titre de la liste et ses tâches
- Clicker sur une liste redirige l'utilisateur vers la page dédiée à cette liste et l'ensemble de ses tâches

## Page dédiée à la liste

- Doit comporter la barre de navigation
- Le titre de la liste
- L'ensemble des tâches
- Chaque tâche possède un bouton pour éditer la tâche et ouvre une modale comportant un input de saisie pour modifier cette tâche, un bouton permettant de valider, un bouton permettant d'annuler
- Chaque tâche possède un bouton pour supprimer cette tâche
- Chaque tâche peut être validée / invalidée
- Un bouton "Ajouter une tâche" ouvrant une modale comportant un input de saisie, un bouton permettant de valider, un bouton permettant d'annuler

## Settings

La page de settings de l'utilisateur comprend:

- La barre de navigation
- Les valeurs des données de l'utilisateur: le nom de l'utilisateur, l'e-mail, le mot de passe
- Les inputs permettant de modifier ces valeurs
- Un bouton permettant de valider l'enregistrement des nouvelles valeurs dans la DB ou d'annuler les modification 
- Au click sur le bouton d'annulation l'utilisateur est redirigé vers la page d'index

