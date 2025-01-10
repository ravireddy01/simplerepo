pipeline {
  agent any
  triggers{
    cron('*/2 * * * *')
  }
  parameters{
    choice(name: 'Environment',choices: ['DEV', 'PROD', 'TEST'], description: 'select specific environment')
  }
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
    stage('input'){
      steps{
        input('Do you want to deploy app in prod')
        echo 'this is waiting for user approval for deploy app in prod'
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
