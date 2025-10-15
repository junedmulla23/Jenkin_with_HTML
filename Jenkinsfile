pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/junedmulla23/Jenkin_with_HTML.git'
            }
        }
        stage('Build') {
            steps {
                echo '🏗️ Building project...'
            }
        }
        stage('Test') {
            steps {
                echo '🧪 Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo '🚀 Deploying application...'
            }
        }
    }

    post {
        success {
            echo '✅ Build completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed! Check logs.'
        }
    }
}

