pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code source recupere depuis GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Compilation des microservices avec Maven'
                sh 'java -version'
                sh 'mvn clean package -DskipTests'
            }
        }
     }
}
