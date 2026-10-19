pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo 'Build completed successfully'
            }
        }

        stage('Automated Testing') {
            steps {
                echo 'Starting automated tests...'

                script {
                    def testResult = 2 + 2

                    if (testResult == 4) {
                        echo 'Test Case 1: PASSED'
                    } else {
                        error 'Test Case 1: FAILED'
                    }

                    def multiplicationResult = 3 * 3

                    if (multiplicationResult == 9) {
                        echo 'Test Case 2: PASSED'
                    } else {
                        error 'Test Case 2: FAILED'
                    }
                }

                echo 'All automated tests passed'
            }
        }

        stage('Deployment') {
            steps {
                echo 'Preparing application for deployment...'
                echo 'Deployment steps executed successfully'
            }
        }
    }

    post {
        success {
            echo 'CI/CD workflow completed successfully'
        }

        failure {
            echo 'CI/CD workflow failed'
        }

        always {
            echo 'Pipeline execution finished'
        }
    }
}

// pipeline {
//     agent any

//     stages {
//         stage('Build') {
//             steps {
//                 echo 'Building the application...'
//             }
//         }

//         stage('Test') {
//             steps {
//                 echo 'Running tests...'
//             }
//         }

//         stage('Deploy') {
//             steps {
//                 echo 'Deploying the application...'
//             }
//         }
//     }
// }
