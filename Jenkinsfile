pipeline {
    agent any
    environment {
        APP_NAME = 'multibranch_test'
    }

    // Stages contain the core logic of the pipeline, organized into logical steps.
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build commands here (e.g., sh 'npm run build' or sh './gradlew build')
                sh 'echo "Doing build stuff.."'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application...'
                // Add your test commands here (e.g., sh 'npm test' or sh './gradlew test')
                sh 'echo "Doing test stuff.."'
            }
        }

        stage('Deliver/Deploy') {
            steps {
                echo 'Preparing for deployment...'
                // Add your deployment commands here (e.g., sh 'kubectl apply -f deployment.yaml')
                sh 'echo "Doing delivery stuff.."'
            }
        }
    }

    // The post section defines actions to run after the pipeline finishes, depending on the outcome.
    post {
        always {
            echo 'This will always run, regardless of the pipeline result.'
        }
        success {
            echo 'This will run only if the pipeline is successful.'
        }
        failure {
            echo 'This will run only if the pipeline fails.'
        }
        cleanup {
            echo 'This will run after all other post conditions.'
        }
    }
}