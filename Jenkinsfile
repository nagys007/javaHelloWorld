pipeline {
    environment {
        def mvnHome = tool 'mvn3'
    }

    agent any

    stages {

        stage('Compile') {
            steps {
                echo "${mvnHome}"
                echo "${mvnHome}\\bin\\mvn.bat clean compile"
                echo bat(returnStdout: true, script: 'set')
                bat "echo hello"
                bat "set PATH"
                bat "set JAVA"
                bat "${mvnHome}\\bin\\mvn.bat clean compile"
            }
        }
        stage('Test') {
            steps {
                echo "${mvnHome}"
                echo "${mvnHome}\\bin\\mvn.bat test"
                bat "${mvnHome}\\bin\\mvn.bat test"
            }
        }
        stage('Package') {
            steps {
                echo "${mvnHome}"
                echo "${mvnHome}\\bin\\mvn.cmd package"
                bat "${mvnHome}\\bin\\mvn.cmd package"
            }
        }
    }
}