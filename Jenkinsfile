pipeline {
    agent any

    def mvnHome = tool 'mvn3'

    stages {
        stage('Compile') {
            steps {
                bat "${mvnHome}\\bin\\mvn clean compile"
            }
        }
        stage('Test') {
            steps {
                bat "${mvnHome}\\bin\\mvn test"
            }
        }
        stage('Package') {
            steps {
                bat "${mvnHome}\\bin\\mvn package"
            }
        }
    }
}