pipeline {
    agent any

    tools {
        // Install the Maven version configured as "mymaven" and add it to the path.
        maven 'mymaven'
    }

    stages {
        stage('compile') {
            steps {
                // Get code from a GitHub repository
                git 'https://github.com/abbadiomer9/DevOpsClassCodes.git'

                // Run Maven on a Unix agent
                sh 'mvn compile'
            }
            post {
                // If the stage is successful
                success {
                    echo 'Compile is successful'
                }
            }
        }

        stage('test') {
            steps {
                // Get code from a GitHub repository
                git 'https://github.com/abbadiomer9/DevOpsClassCodes.git'

                // Run Maven tests
                sh 'mvn test'
            }
            post {
                // If the stage is successful
                success {
                    echo 'Test is successful'
                }
            }
        }

        stage('package-create') {
            steps {
                // Get code from a GitHub repository
                git 'https://github.com/abbadiomer9/DevOpsClassCodes.git'

                // Run Maven package
                sh 'mvn package'
            }
            post {
                // If the stage is successful
                success {
                    echo 'Package creation is successful'
                }
            }
        }
    }
}
