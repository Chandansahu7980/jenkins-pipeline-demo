pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the application..."
                sh "echo Build Stage Complete"
            }
        }

        stage('Test') {
            steps {
                echo "Running Tests..."
                sh "echo Test Stage OK"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying..."
                sh "echo Dummy Deployment Done"
            }
        }
    }
}
