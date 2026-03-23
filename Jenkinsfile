pipeline {
    agent any
    
    tools {
        maven 'Maven3' // Matches your Jenkins Global Tool Configuration [cite: 173]
    }

    stages {
        stage('Checkout') {
            steps {
                // ADDED 'branch: main' here to fix the "Couldn't find any revision" error
                git branch: 'main', url: 'https://github.com/AbhishekPawar-1904/maven.git' 
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install' // Correct for Windows as per your manual 
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
