pipeline {
    agent { docker 'python:3.5.1' }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh 'echo "Hello ${BRANCH_NAME}"'
            }
        }
    }
    post {
        always {
            echo "This will always run"
        }
        success {
            echo "This will only run if success"
        }
        failure {
            echo "This will only run if failure"
        }
    }
}
