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
                    emailext body:'Summary',subject:'Pipeline Status',to:'archana.sandbhorsv@gmail.com'
                }
            }
}
                
