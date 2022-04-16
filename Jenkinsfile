pipeline {
  agent any
  environment {
    ENV_URL="roboshop.internal.com"
  }
  stages {
    stage('Stage View1') {
        steps {
            echo 'Hello friends, welcome to Jenkins'
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




