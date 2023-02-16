pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cpp -o PES1UG20CS495'
                jenkinsBuild job: 'PES1UG20CS495-1', wait: true
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS495'
            }
        }
        stage('Deploy') {
            steps {
                // add deployment steps here
            }
        }
    }

    post {
        always {
            echo "Pipeline completed."
        }
        failure {
            echo "Pipeline failed."
        }
    }
}
