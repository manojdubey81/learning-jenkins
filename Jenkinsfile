pipeline {
  agent any

  environment {
    ENV_URL = "pipeline.google.com"
  }

  stages {

    stage('Two') {
      steps {
        echo "Two"
        sh 'echo ENV_URL = ${ENV_URL}'
      }
    }
  }
}

