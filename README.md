# 📊 Lab 1 : Suivi des Scripts des Développeurs (JDBC)

## 📝 Présentation
Ce projet constitue une introduction pratique à la manipulation de bases de données relationnelles avec **Java JDBC**. L'objectif est de suivre la production quotidienne de scripts au sein d'une équipe de développeurs et d'en extraire des statistiques décisionnelles.

## 🎯 Objectifs Pédagogiques
* **Connexion MySQL** : Établir un pont entre Java et MySQL via le driver JDBC.
* **Manipulation SQL** : Création de tables, insertion de données et requêtes d'agrégation directement depuis le code Java.
* **Sécurité & Performance** : Utilisation de `Statement` pour les requêtes simples et de `PreparedStatement` pour les requêtes paramétrées (protection contre l'injection SQL).
* **Analyse de données** : Utilisation de fonctions SQL avancées (`GROUP BY`, `SUM`, `MAX`, `ORDER BY`).



## 🏗️ Structure du Programme
Le programme `ExoJDBC.java` suit un flux logique rigoureux :
1. **Chargement du Driver** : Initialisation du connecteur MySQL.
2. **Gestion de la Connexion** : Utilisation du bloc *try-with-resources* pour garantir la fermeture propre de la connexion.
3. **Initialisation du Schéma** : Réinitialisation de la table `DevData` pour assurer un environnement de test propre.
4. **Calcul des Statistiques** :
    * Recherche de la performance maximale par jour.
    * Classement des développeurs par productivité totale.
    * Calcul de la production globale de la semaine.
    * Recherche filtrée par développeur (via `PreparedStatement`).

## 🛠️ Configuration Requise
* **Base de données** : MySQL (Workbench ou XAMPP).
* **Environnement** : JDK 11+ et un IDE (NetBeans, IntelliJ ou Eclipse).
* **Dépendance** : `mysql-connector-j-8.x.x.jar` ajouté au Build Path du projet.

## ⚙️ Installation Rapide
1. **SQL** : Créer la base de données avec `CREATE DATABASE atelier;`.
2. **Java** : Adapter les constantes `USER` et `PASSWORD` dans le fichier source selon votre configuration locale.
3. **Exécution** : Lancer la classe `ExoJDBC.java`.

## ✅ Résultats Attendus
Une exécution réussie affiche dans la console :
* Le statut de la connexion.
* La confirmation de la création des données.
* Quatre blocs de statistiques détaillées (Max par jour, Classement, Total Semaine, Total Individuel).

<img width="856" height="423" alt="lab1" src="https://github.com/user-attachments/assets/2852cb78-ffa6-436c-837d-b41f2ed304ca" />

<img width="772" height="325" alt="bdlab1" src="https://github.com/user-attachments/assets/7780cd8d-8f1c-4673-958c-98165becc384" />



# 🛠️ Lab 2 : Gestion des Machines et Employés (JDBC)

## 📝 Présentation
Ce projet est une application de gestion de parc technique réalisée en **Java**. Elle permet de gérer les employés et d'affecter des machines à chacun d'entre eux. L'accent a été mis sur une architecture robuste et une gestion propre de la base de données **MySQL**.

## 🏗️ Points clés du projet
* **Architecture en couches** : Séparation stricte entre les Entités, le DAO (*Data Access Object*) et la couche Service pour une meilleure maintenance.
* **Design Pattern Singleton** : Utilisation d'une instance unique pour gérer la connexion à la base de données, optimisant ainsi l'utilisation des ressources système.
* **Relations 1:N** : Gestion complète du lien logique et physique entre un employé et ses multiples machines.
* **Intégrité des données** : Mise en place de la suppression en cascade (*ON DELETE CASCADE*) : si un employé est supprimé, toutes ses machines associées le sont automatiquement.



## 📂 Structure du projet
Le projet est organisé selon les packages suivants :
* **`entities`** : Définition des objets métiers (`Employe`, `Machine`).
* **`dao`** : Logique d'accès à la base de données et exécution des requêtes SQL.
* **`service`** : Orchestration des données et implémentation de la logique métier.
* **`util`** : Utilitaires système et configuration de la connexion JDBC (Classe `Connexion`).
* **`app`** : Classes de tests (`main`) pour valider les fonctionnalités CRUD.

## 💻 Installation
1. **Base de données** : Importer le script SQL ou créer les tables via **XAMPP / phpMyAdmin**.
2. **Bibliothèques** : Ajouter le connecteur `mysql-connector-j-8.x.x.jar` dans les bibliothèques du projet NetBeans.
3. **Exécution** : Lancer les fichiers de test `TestEmploye.java` ou `TestMachine.java` pour vérifier le bon fonctionnement du système.

<img width="910" height="306" alt="lab2test" src="https://github.com/user-attachments/assets/791396ef-a734-450b-97bd-9c406bc2819b" />

<img width="914" height="285" alt="lab2Machinetest" src="https://github.com/user-attachments/assets/b848441c-7477-48c7-943f-4294e5dd4f70" />

<img width="720" height="189" alt="basedoneelab2" src="https://github.com/user-attachments/assets/379a0371-cd74-4343-8fb4-9484c386bdbe" />

