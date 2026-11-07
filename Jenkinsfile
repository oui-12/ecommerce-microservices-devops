pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code source recupere depuis GitHub'
            }
        }

        stage('Build') {
            agent {
                docker {
                    image 'maven:3.9-eclipse-temurin-25'
                }
            }
            steps {
                echo 'Compilation des microservices avec Maven'
                sh 'java -version'
                sh 'mvn -version'
                sh 'mvn clean package -DskipTests'
            }
        }
     }
}
