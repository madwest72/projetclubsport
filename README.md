# Mouvement Maximal - Plateforme Web du Club de Sport

Bienvenue sur le dépôt du projet "Mouvement Maximal", une application web développée en binôme dans le cadre de la 1ère année de BTS SIO (option SLAM). 

Ce projet a pour but de fournir une plateforme complète pour un club omnisports virtuel, incluant une vitrine pour les utilisateurs et un back-office (espace administrateur) pour la gestion des adhérents et le suivi des statistiques.

## Objectifs du projet (Travail de groupe)

- Collaboration : Se répartir les tâches de développement (Front-end / Back-end / Base de données) et coordonner l'intégration du code.
- Conception de données : Modélisation préalable de la base de données (MCD) avant l'implémentation.
- Design UI/UX : Créer une identité visuelle forte (thème sombre avec accents orange) et une interface utilisateur claire pour présenter les différentes disciplines.
- Gestion des données (CRUD) : Permettre l'inscription de nouveaux membres et le suivi des effectifs via une base de données relationnelle.
- Espace sécurisé : Mettre en place un espace administration restreint pour gérer le club.

## Technologies utilisées

- Back-end : PHP 8, PDO
- Base de données : MySQL / MariaDB
- Front-end : HTML5, CSS3, (Bootstrap pour la structure)
- Conception : Looping (Modélisation de données)
- Environnement : Serveur local (XAMPP/WAMP)

## Architecture de l'application

Le code est rigoureusement séparé en trois dossiers distincts pour la logique métier, la gestion des données et l'interface publique :

```text
projetclubsport/
│
├── admin/                  # ESPACE ADMINISTRATION (Accès restreint)
│   ├── commun/             # Composants partagés du back-office
│   │   ├── footer.php
│   │   └── header.php
│   ├── formulaire.php      # Formulaire d'ajout d'un nouvel adhérent
│   ├── stat.php            # Tableau de bord : statistiques de remplissage par sport
│   └── user.php            # Liste et gestion des utilisateurs inscrits
│
├── BDD/                    # GESTION DE LA BASE DE DONNÉES
│   ├── bdd.php             # Script de connexion PDO
│   └── script.sql          # Script de création des tables
│
├── vitrine/                # ESPACE PUBLIC (Côté utilisateur)
│   ├── commun2/            # Composants partagés du front-office
│   │   ├── footer1.php
│   │   └── header1.php
│   ├── img/                # Ressources graphiques
│   ├── index.php           # Page d'accueil (Actualités, Nouveautés)
│   ├── athle.php           # Page section Athlétisme
│   ├── basket.php          # Page section Basketball
│   ├── danse.php           # Page section Danse
│   ├── foot.php            # Page section Football
│   ├── natation.php        # Page section Natation
│   ├── contact.php         # Informations de contact
│   ├── info.php            # Informations générales du club
│   ├── inscription.php     # Modalités d'inscription
│   ├── login.php           # Page de connexion à l'administration
│   └── style.css           # Feuille de style du site
│
├── mcdsport.loo            # Fichier de modélisation conceptuelle (Looping)
├── mcdsport.lo1            # Fichier de modélisation associé
└── readme                  # Documentation du projet