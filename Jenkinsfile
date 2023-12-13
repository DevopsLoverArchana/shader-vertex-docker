pipeline{
    agent any
  stages{
    stage('build'){
      steps{
        echo 'building the pipeline application'
      }
    }
    stage('Test'){
      steps{
        echo 'Running test'
      }
    }
     stage('Deploy'){
      steps{
        echo 'Deploying the application'
      }
    }
  }
  post{
    sucess{
      echo 'my pipeline sucess'
    }
    failuare{
      echo 'pipeline failed'
    }
  }
}
   
