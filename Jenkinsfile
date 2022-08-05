pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Building the application'
            }
        }
        stage('test') {
            steps {
                echo 'Testing the application'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploy the application'
            }
        }
    }

    post {
        always {
            emailext body: 'Check console output at $BUILD_URL to view the results.', 
                    to: "nihalcyberdude@gmail.com", 
                    subject: 'Unstable build in Jenkins'
        }
    }
}
