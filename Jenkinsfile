pipeline {
    agent any
    tools {
        nodejs 'nodejs' // Utilisation de Node.js configuré dans Jenkins
    }

    stages {
        stage('Check NPM Version') {
            steps {
                script {
                    // Vérifier la version de npm avec l'environnement nodejs
                    sh 'npm version'
                }
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Installer les dépendances via npm
                    sh 'npm install'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'npm start server.js'  
            }
        }
    }
}