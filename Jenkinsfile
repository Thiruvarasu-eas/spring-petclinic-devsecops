pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Thiruvarasu-eas/spring-petclinic-devsecops.git'
            }
        }

        stage('Build') {
            steps {
                bat '.\\mvnw.cmd clean compile'
            }
        }

        stage('Test') {
            steps {
                bat '.\\mvnw.cmd test'
            }
        }

        stage('Package') {
            steps {
                bat '.\\mvnw.cmd package'
            }
        }
    }
}