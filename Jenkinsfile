pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Swethsira/gitjenkinsinstegration.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java program...'
                bat 'javac sample.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program...'
                bat 'java sample'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
