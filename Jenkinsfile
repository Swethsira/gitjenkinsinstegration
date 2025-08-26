pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Swethsira/gitjenkinsinstegration/new/master'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java program...'
                bat 'javac Sample.java'
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
