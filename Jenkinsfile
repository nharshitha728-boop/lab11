pipeline {

    agent any

    tools {
        jdk 'JDK17'
        maven 'Maven3'
    }

    stages {

        stage('Checkout') {

            steps {
                git 'https://github.com/nharshitha728-boop/lab11.git'
            }
        }

        stage('Build') {

            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {

            steps {
                sh 'mvn test'
            }
        }
    }

    post {

        always {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}