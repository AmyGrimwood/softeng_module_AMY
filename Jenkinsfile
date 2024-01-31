pipeline {
    agent {
        docker {
            image "docker:24.0.6-git" // Set docker image
        }
    }

    stages {
        stage('Build') {
            steps {
                // In this stage, you can put commands to build your project.
                sh 'echo "Building the project..."'
            }
        }

        stage('Test') {
            steps {
                // In this stage, you can put commands to run tests.
                sh 'echo "Running tests..."'
            }
        }
    }

    post {
        success {
            // This block is executed if the pipeline runs successfully.
            echo 'Pipeline succeeded! Your project is built and tested.'
        }
        failure {
            // This block is executed if the pipeline fails.
            echo 'Pipeline failed. Please check the logs for details.'
        }
    }
}