# devops
Nom du Projet: Pipeline CI/CD avec Jenkins, Maven, SonarQube, Nexus et Docker

Résumé: Ce projet met en place un pipeline CI/CD complet utilisant Jenkins, Maven, SonarQube, Nexus et Docker. Le pipeline est conçu pour automatiser les étapes de compilation, de test, d’analyse de code, de déploiement et de déploiement avec Docker. Le projet a été développé et testé dans un environnement Vagrant.

Technologies Utilisées:

Jenkins: Pour l’automatisation du pipeline CI/CD.
Maven: Pour la gestion des dépendances et la compilation du projet.
SonarQube: Pour l’analyse de la qualité du code.
Nexus: Pour le déploiement des artefacts.
Docker: Pour la construction et le déploiement des conteneurs.
Vagrant: Pour la gestion de l’environnement de développement.
Étapes du Pipeline:

Git Checkout: Récupération du projet depuis le dépôt Git.
Compile: Compilation du projet avec Maven.
Run Tests: Exécution des tests unitaires.
SonarQube Analysis: Analyse de la qualité du code avec SonarQube.
Nexus Deployment: Déploiement des artefacts sur Nexus.
Build and Deploy with Docker: Construction et déploiement des conteneurs Docker.
Configuration:

Jenkinsfile: Fichier de configuration du pipeline Jenkins.
Vagrantfile: Fichier de configuration de l’environnement Vagrant.
Instructions:

Cloner le dépôt Git.
Configurer les variables d’environnement dans Jenkins.
Exécuter le pipeline Jenkins pour automatiser le processus de CI/CD.
