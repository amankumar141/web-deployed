pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from your repository
                git 'https://github.com/amankumar141/web-deployed'
            }
        }

        stage('Build') {
            steps {
                echo 'No build step needed for static HTML'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying index.html to web server...'
                // Replace /var/www/html with your actual web server path
                sh 'cp index.html /var/www/html/index.html'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful!'
        }
        failure {
            echo 'Deployment failed.'
        }
    }
}