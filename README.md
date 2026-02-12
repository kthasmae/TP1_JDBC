📊 Lab 1 : Suivi des Scripts des Développeurs (JDBC)
📝 Présentation
Ce projet constitue une introduction pratique à la manipulation de bases de données relationnelles avec Java JDBC. L'objectif est de suivre la production quotidienne de scripts au sein d'une équipe de développeurs et d'en extraire des statistiques décisionnelles.

🎯 Objectifs Pédagogiques
Connexion MySQL : Établir un pont entre Java et MySQL via le driver JDBC.

Manipulation SQL : Création de tables, insertion de données et requêtes d'agrégation directement depuis le code Java.

Sécurité & Performance : Utilisation de Statement pour les requêtes simples et de PreparedStatement pour les requêtes paramétrées (sécurité contre l'injection SQL).

Analyse de données : Utilisation de fonctions SQL avancées (GROUP BY, SUM, MAX, ORDER BY).

🏗️ Structure du Programme
Le programme ExoJDBC.java suit un flux logique rigoureux :

Chargement du Driver : Initialisation du connecteur MySQL.

Gestion de la Connexion : Utilisation du bloc try-with-resources pour garantir la fermeture propre de la connexion.

Initialisation du Schéma : Réinitialisation de la table DevData pour assurer un environnement de test propre.

Calcul des Statistiques :

Recherche de la performance maximale par jour.

Classement des développeurs par productivité totale.

Calcul de la production globale de la semaine.

Recherche filtrée par développeur (via PreparedStatement).

🛠️ Configuration Requise
Base de données : MySQL (Workbench ou XAMPP).

Environnement : JDK 11+ et un IDE (NetBeans, IntelliJ ou Eclipse).

Dépendance : mysql-connector-j-8.x.x.jar ajouté au Build Path du projet.

⚙️ Installation Rapide
SQL : Créer la base de données avec CREATE DATABASE atelier;.

Java : Adapter les constantes USER et PASSWORD dans le fichier source selon votre configuration locale.

Exécution : Lancer la classe ExoJDBC.java.

✅ Résultats Attendus
Une exécution réussie affiche dans la console :

Le statut de la connexion.

La confirmation de la création des données.

Quatre blocs de statistiques détaillées (Max par jour, Classement, Total Semaine, Total Individuel).

<img width="856" height="423" alt="lab1" src="https://github.com/user-attachments/assets/2852cb78-ffa6-436c-837d-b41f2ed304ca" />

<img width="772" height="325" alt="bdlab1" src="https://github.com/user-attachments/assets/7780cd8d-8f1c-4673-958c-98165becc384" />



🛠️ Gestion des Machines et Employés (JDBC)
📝 Présentation
Ce projet est une application de gestion de parc technique réalisée en Java. Elle permet de gérer les employés et d'affecter des machines à chacun d'entre eux. L'accent a été mis sur une architecture robuste et une gestion propre de la base de données MySQL.

🏗️ Points clés du projet
Architecture en couches : Séparation stricte entre les Entités, le DAO (Data Access Object) et la couche Service.

Design Pattern Singleton : Utilisation d'une instance unique pour gérer la connexion à la base de données, optimisant ainsi les ressources.

Relations 1:N : Gestion complète du lien entre un employé et ses multiples machines.

Intégrité des données : Mise en place de la suppression en cascade (si un employé est supprimé, ses machines le sont aussi).

📂 Structure du projet
entities : Définition des objets métiers.

dao : Logique d'accès à la base de données (Requêtes SQL).

service : Orchestration des données et logique métier.

util : Utilitaires système et configuration de la connexion.

app : Classes de tests pour valider les fonctionnalités.

💻 Installation
Importer la base de données via XAMPP/phpMyAdmin.

Ajouter le connecteur JDBC MySQL dans les bibliothèques du projet NetBeans.

Lancer les fichiers de test (TestEmploye.java ou TestMachine.java) pour vérifier le bon fonctionnement.

<img width="910" height="306" alt="lab2test" src="https://github.com/user-attachments/assets/791396ef-a734-450b-97bd-9c406bc2819b" />

<img width="914" height="285" alt="lab2Machinetest" src="https://github.com/user-attachments/assets/b848441c-7477-48c7-943f-4294e5dd4f70" />

<img width="720" height="189" alt="basedoneelab2" src="https://github.com/user-attachments/assets/379a0371-cd74-4343-8fb4-9484c386bdbe" />

