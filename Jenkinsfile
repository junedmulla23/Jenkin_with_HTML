pipeline {
    agent any
    environment {
        DEPLOY_DIR = 'C:\\inetpub\\wwwroot'  // for IIS
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning project from GitHub...'
                git branch: 'main', url: 'https://github.com/<your-username>/Jenkin_with_HTML.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Build Step: Checking workspace files'
                bat 'dir'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing HTML syntax...'
                bat 'echo HTML validation step (dummy)'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying index.html to IIS folder"
                bat "xcopy /Y index.html ${DEPLOY_DIR}\\"
            }
        }
    }
    post {
        success {
            echo '✅ Pipeline finished successfully! Visit http://localhost/index.html'
        }
        failure {
            echo '❌ Pipeline failed! Check logs.'
        }
    }
}
