TP 5 : Intégration de Spring et Hibernate
Titre : TP 5 – Intégration de Spring et Hibernate
Objectif :

L’objectif de ce TP est de mettre en place une application Java utilisant Spring pour l’injection de dépendances et la gestion des transactions, et Hibernate pour la gestion du mapping objet-relationnel (ORM). On apprend à configurer un projet Maven, définir des entités JPA et créer des DAO génériques pour manipuler les données dans une base MySQL.

Étapes réalisées :
1. Création du projet Maven

Un projet Maven nommé spring-hibernate-demo a été créé dans l’IDE.

La structure du projet a été organisée en plusieurs packages :

dao : contient les interfaces et classes d’accès aux données.

entities : contient les entités JPA représentant les tables de la base de données.

metier : contient la logique métier de l’application.

util : pour les utilitaires et la configuration.

Les ressources, comme le fichier de configuration, se trouvent dans le dossier resources.

2. Ajout des dépendances Maven

Les dépendances nécessaires pour Spring et Hibernate ont été ajoutées dans le fichier pom.xml :

spring-context : pour l’injection de dépendances.

spring-orm : pour l’intégration Spring-Hibernate.

hibernate-core : pour le mapping objet-relationnel.

mysql-connector-java : pour connecter l’application à MySQL.

spring-tx : pour la gestion automatique des transactions.

validation-api : pour la validation des entités via JPA.

Explication : ces dépendances permettent de créer une application modulable, facilement configurable et connectée à une base de données MySQL.

3. Création de l’entité Product

Une entité Product a été définie dans le package entities.

Cette entité contient les attributs id, name et price.

Les annotations JPA sont utilisées pour :

Indiquer que c’est une entité.

Définir la clé primaire et la génération automatique de l’identifiant.

4. Création de l’interface DAO générique

Une interface générique IDao<T> a été créée dans le package dao.

Elle définit les méthodes CRUD communes pour toutes les entités :

Création, suppression, mise à jour.

Recherche par identifiant et récupération de tous les enregistrements.

Cette interface permet de standardiser l’accès aux données et de réutiliser le code pour différentes entités.
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-03-10 010157" src="https://github.com/user-attachments/assets/9334673c-149a-4985-93f0-cf0e1dab8577" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-03-10 010132" src="https://github.com/user-attachments/assets/3c8227f4-2a12-4193-b4de-7d0313d60c42" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-03-10 010056" src="https://github.com/user-attachments/assets/e24a142f-fc5f-4825-b1fb-fb8d4df7b96b" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-03-10 005924" src="https://github.com/user-attachments/assets/7fe3fd02-8b83-4195-b5b1-580760523e3b" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-03-10 005915" src="https://github.com/user-attachments/assets/2a734929-8d63-42e9-8cfc-d1fba2a4a8cc" />
