pipeline {
    agent {
        docker { image 'python:3.11-slim' } // Utilise une image Docker avec Python
    }

    stages {
        stage('Run tests') {
            steps {
                sh 'python3 test_calculs.py' // Lance les tests
            }
        }
    }

    post {
        success {
            echo 'Pipeline terminé avec succès !'
        }
        failure {
            echo 'Pipeline échoué !'
        }
    }
}

