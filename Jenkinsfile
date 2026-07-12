pipeline {
    agent any
    tools {
        jdk 'JDK11' // Keep your Java tool definition intact
    }
    stages {
        stage('Git Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build & Package') {
            steps {
                // Change 'mvn' to './mvnw' to use the local project wrapper
                sh './mvnw clean package -DskipTests'
            }
        }
    }
}
