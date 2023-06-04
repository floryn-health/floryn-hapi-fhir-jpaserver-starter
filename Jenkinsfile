pipeline {
    agent any
    
    tools {
        maven 'Maven 3.9.2' // Specify the name of the configured Maven installation
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system (e.g., Git)
                checkout scm
            }
        }

        stage('Clean') {
            steps {
                // Clean the Maven project
                sh 'mvn clean'
            }
        }

        stage('Build') {
            steps {
                // Build the Maven project and create the artifact
                sh 'mvn install'
            }
        }
    }
}
