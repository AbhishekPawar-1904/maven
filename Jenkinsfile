pipeline {
    agent any
    
    tools {
        maven 'Maven3' // This must match the name you gave in Jenkins Tools
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/AbhishekPawar-1904/maven.git' 
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install' // Use 'bat' for Windows, 'sh' for Linux
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
