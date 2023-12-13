pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'build application'
            }
        }

        stage('Test') {
            steps {
                echo 'test application'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy application'
            }
            post {
                success {
                    emailext(
                        subject: "Deployment Successful",
                        body: "Your deployment was successful.",
                        to: "archana.sandbhorsv@gmail.com",
                        attachLog: true,
                        mimeType: 'text/html' // Optionally specify MIME type
                    )
                }
                failure {
                    emailext(
                        subject: "Deployment Failed",
                        body: "Your deployment has failed. Please check the Jenkins logs.",
                        to: "archana.sandbhorsv@gmail.com",
                        attachLog: true,
                        mimeType: 'text/html' // Optionally specify MIME type
                    )
                }
            }
        }
    }
}
