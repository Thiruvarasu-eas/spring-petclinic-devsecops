pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh './mvnw clean compile'
            }
        }

        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Package') {
            steps {
                sh './mvnw package'
            }
        }
        stage('Code Coverage') {
            steps {
                 sh './mvnw jacoco:report'
            }
        }
        stage('Dependency Check') {
            steps {
                 sh './mvnw org.owasp:dependency-check-maven:check'
            }
        }
    }
}