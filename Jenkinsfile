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
 		    sh 'npm install -g pm2'
                }
            }
        }
       
	stage('Verify PM2 process') {
            steps {
                sh 'pm2 list'
            }
        }

        stage('Deploy') {
            steps {
                sh 'pm2 start server.js'  
            }
        }
    }
}
