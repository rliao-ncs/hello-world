pipeline {
    agent any

    tools {
        maven 'Default' // This should match the name of the Maven installation in Jenkins
        jdk 'Default'   // This should match the name of the JDK installation in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build steps here, e.g., bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test steps here, e.g., bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging...'
                // Add your package steps here, e.g., bat 'mvn package'
                bat 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy steps here, e.g., bat 'docker run ...'
                bat 'java -cp target/hello-world-1.0-SNAPSHOT.jar com.example.App'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}