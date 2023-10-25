pipeline {
    agent any
    tools { // Spécifiez les outils ici
        nodejs 'Built-In Node'
    }
    triggers {
        pollSCM('*/5 * * * *') // Vérifier toutes les 5 minutes
    }
    stages {
        stage('Checkout') {
            steps {
                echo "Récupération du code source"
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Build du projet"
                // Ajoutez les commandes de build ici
            }
        }
        stage('Deploy') {
            steps {
                echo "Déploiement du projet"
                // Ajoutez les commandes de déploiement ici
            }
        }
        stage('Execute app.js') {
            steps {
                echo "Exécution du fichier app.js"
                // Remplacez la commande suivante par l'exécution de votre fichier JavaScript
                sh 'node app.js' // Cette commande exécute le fichier app.js avec Node.js
            }
        }
    }
}
