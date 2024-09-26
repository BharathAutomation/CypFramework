pipeline{
    agent any

    stages{
        stage('Install Required dependency packages') {
            steps {
                bat 'npm install'
            }
        }

        stage('Executing the test scripts and generating test report') {
            steps {
                bat 'npm run test-suite'
            }
        }
    }

    post{
        always{
            echo 'Test Execution completed and check the test results under workspace'
        }
    }
}