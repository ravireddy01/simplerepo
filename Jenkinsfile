pipeline {
  agent any
  stages{
    stage('git-code'){
      steps{
        echo 'code checkout'
      }
    }
     stage('build'){
      steps{
        echo 'code build'
      }
    }
     stage('test-code'){
      steps{
        echo 'code testing'
      }
    }
     stage('pre-prod'){
      steps{
        echo 'app in pre-prod'
      }
    }
     stage('prod'){
      steps{
        echo 'app in prod'
      }
    }
  }
  post{
    success{
      echo 'app is successfully deploy in prod'
    }
    failure{
      echo "app isn't deploy in prod"
    }
  }
}
