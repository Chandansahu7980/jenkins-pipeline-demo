pipeline {
    agent any

    parameters {
        choice(name:'ENV', choices: ['dev','test'], description: 'Select Environment')
        booleanParam(name:'DEBUG_MODE', defaultValue: false, description: 'Enable debug logs?')
        string(name:'VERSION', defaultValue:'1.0.0', description: 'App Version')
    }

    stages {
        stage('show parameters'){
            steps{
                echo "Deploying to: ${params.ENV}"
                echo "Debug Mode: ${params.DEBUG_MODE}"
                echo "Version: ${params.VERSION}"
            }
        }
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
                script{
                    if (params.ENV == 'dev') {
                        echo "Deploying to DEV Environment..."
                    } else {
                        echo "Deploying to TEST Enviornment..."
                    }
                }
            }
        }
    }
}
