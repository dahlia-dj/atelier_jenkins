pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps {
                    echo 'Repository cloned'
                }
            }
       
        stage ('Run Python') {
            steps {
                    sh 'cat app.py'

            }
        }

        stage('Install dependencies') {
            steps {
                echo 'Étape 1 : Installation des dépendances'
                sh 'pip install -r requirements.txt' 
            }
        }
        stage('Tests') {
            steps {
                echo 'Étape 2 : Exécution des tests automatisés avec Pytest'
                sh 'pytest'
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

        stage ('Test DAG syntax') {
            steps {
                    sh 'py -m py_compile sales_pipeline .py'
            }
        }

        stage ('Deploy DAG') {
            steps {
                    sh 'cp sales_pipeline .py /opt/airflow/dags/'
            }
        }

        stage ('Trigger DAG') {
            steps {
                    sh 'airflow dags trigger sales_pipeline'
            }
        }
    }
}