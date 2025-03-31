pipeline {
    agent any

    environment {
        NODEJS_HOME = '/usr/local/bin/node'  // Ajustez si nécessaire
        PATH = "${NODEJS_HOME}:${env.PATH}"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh '/usr/bin/local/pm2 start server.js'  // Ou autre commande de déploiement
            }
        }
    }
}

