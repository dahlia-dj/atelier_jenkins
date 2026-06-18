pipeline {
    agent any
    stages {
        stage('Install dependencies') {
            steps {
                echo 'Étape 1 : Installation des dépendances'
                //sh 'pip install -r requirements.txt' 
            }
        }
        stage('Tests') {
            steps {
                echo 'Étape 2 : Exécution des tests automatisés avec Pytest'
                //sh 'pytest'
            }
        }
        stage('Build Docker Image') {
            steps {
                echo 'Étape 3 : Construction de limage Docker'
               // sh 'docker build -t myapp .' 
            }
        }
        stage('Run Docker Container') {
            steps {
                echo 'Étape 4 : Lancement du conteneur de test'
                //sh 'docker run myapp'
            }
        }
    }
}