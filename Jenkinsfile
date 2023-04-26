pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                sh "mvn clean compile"

            }
        }

        stage('Test') {
                    steps {
                        // Get some code from a GitHub repository
                        sh "mvn test"

                    }
                }

        stage('Deploy') {
                    steps {
                        // Get some code from a GitHub repository
                        sh "mvn heroku:deploy"

                    }
                }
    }
}
