pipeline {
    agent any
    tools {
        jdk 'JDK11' // This maps to your Java 21 tool configuration in Jenkins
    }
    stages {
        stage('Git Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build & Package') {
            steps {
                // Compile and skip tests to keep execution lightning fast
                sh 'mvn clean package -DskipTests'
            }
        }
    }
}
