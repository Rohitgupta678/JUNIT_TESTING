pipeline {
    agent any

    tools {
        JDK 'JDK8'
        maven 'Maven'   // Make sure Maven is configured in Jenkins
    }

    stages {

        stage('Checkout') {
            steps {
                checkout https://github.com/Rohitgupta678/JUNIT_TESTING/edit/main/Jenkinsfile#LL4
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
