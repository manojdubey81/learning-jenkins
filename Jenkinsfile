pipeline {
  agent any
  environment {
    ENV_URL="google.com"
  }
  parameters{
    string (name: 'PERSON', defaultValue: 'Mr Manoj', description: 'I am pro devops guy')
  }
  stages {
    stage('Stage View1') {
        environment {
            ENV_URL="yahoo.com"
        }
        steps {
            echo "Hello ${params.PERSON}"
            sh 'echo ENV_URL=${ENV_URL}'
        }
    }
    stage('Stage View2') {
        steps {
            sh 'echo ENV_URL=${ENV_URL}'
        }
    }
  }
  post{
    always {
        echo 'I will always say Hello again!'
    }
    changed {
        echo 'I will always say Only changed result!'
    }
    fixed {
        echo 'I will always say Hello always!'
    }
  }
}




