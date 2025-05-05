pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Running Build Step...'
                sh 'python3 f1.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Test Step...'
                sh 'python3 f2.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Running Deploy Step...'
                sh 'python3 f3.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs.'
        }
    }
}
