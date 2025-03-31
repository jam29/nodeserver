pipeline {
    agent any

    environment {
        NODEJS_HOME = '/usr/local/bin/node'  // Ajustez si nécessaire
        PATH = "${NODEJS_HOME}:${env.PATH}"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh '/usr/local/bin/npm install'
            }
        }

        stage('Test') {
            steps {
                sh '/usr/local/bin/npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh '/usr/bin/local/node server.js'  // Ou autre commande de déploiement
            }
        }
    }
}

