pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cpp -o PES1UG20CS495'
                build job: 'PES1UG20CS495-1', wait: false
                echo 'Build Successful'
            }
        }
        stage('Test') {
            steps {
                sh 'cat working.cpp'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployment Successful";
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
