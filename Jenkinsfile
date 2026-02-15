pipeline {
    agent any

    stages {
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
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}
