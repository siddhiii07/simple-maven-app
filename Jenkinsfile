pipeline {
    agent any

    tools {
        maven 'Maven 3.9.9' // Use your Maven version
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/siddhiii07/simple-maven-app.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
        success {
            echo 'Build and Test successful'
        }
        failure {
            echo 'Build or Test failed'
        }
    }
}
