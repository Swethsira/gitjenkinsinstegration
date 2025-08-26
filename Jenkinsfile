pipeline {
    agent any

    stage('Run') {
    steps {
        echo 'Running Java program...'
        bat 'java Sample'
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
