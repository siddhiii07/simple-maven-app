pipeline {
    agent any 

    tools {
        maven 'apache maven' // Use the correct Maven name
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean package' // Replace with your actual build command
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test' // Replace with your actual test command
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment commands here
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
