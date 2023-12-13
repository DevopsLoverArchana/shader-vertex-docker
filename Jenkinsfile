pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Your build steps here
            }
        }

        stage('Test') {
            steps {
                // Your test steps here
            }
        }

        stage('Deploy') {
            steps {
                // Your deployment steps here
            }
            post {
                success {
                    // Send an email on successful deployment
                    emailext(
                        subject: "Deployment Successful",
                        body: "Your deployment was successful.",
                        to: "archana.sandbhorsv@gmail.com",
                        attachLog: true
                    )
                }
                failure {
                    // Send an email if deployment fails
                    emailext(
                        subject: "Deployment Failed",
                        body: "Your deployment has failed. Please check the Jenkins logs.",
                        to: "archana.sandbhorsv@gmail.com",
                        attachLog: true
                    )
                }
            }
        }
    }
}
