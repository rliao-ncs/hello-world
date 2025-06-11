pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build steps here, e.g., sh 'mvn clean install'
				bat 'mvn clean install'
				bat 'mvn package'
			}
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test steps here, e.g., sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy steps here, e.g., sh 'docker run ...'
				bat 'java -cp target/hello-world-1.0-SNAPSHOT.jar com.example.App'
            }
        }
    }
}