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
        }
    }
            post {
                always
                {
                    mail to :"archana.sandbhorsv@gmail.com",
                        subject:"sending and testing email",
                        body:"Test"
                }
            }
}
                
