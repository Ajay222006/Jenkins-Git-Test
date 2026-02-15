pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Ajay222006/Jenkins-Git-Test.git'
            }
        }

        stage('Compile') {
            steps {
                bat 'javac Hello.java'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '*.class'
            }
        }
    }

    post {
        failure {
            echo 'Build Failed!'
        }
        success {
            echo 'Build Successful!'
        }
    }
}
