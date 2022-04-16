pipeline {
  agent any
  environment {
    ENV_URL="google.com"
  }
//  parameters{
//   string (name: 'PERSON', defaultValue: 'Mr Manoj', description: 'I am pro devops guy')
//   text(name: 'BIOGRAPHY', defaultValue: 'Cricket', description: 'Enter some information about the person')
//   booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//   choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//   password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
// }
// triggers {
//   cron('H/1 * * * *')
// }
  stages {
    stage('Stage View1') {
        environment {
            ENV_URL="yahoo.com"
        }
        steps {
           // echo "Hello ${params.PERSON}"
           // echo "Biography: ${params.BIOGRAPHY}"
            sh 'echo ENV_URL=${ENV_URL}'
        }
    }
    stage('Stage View2') {
        input {
             message "Should we continue?"
             ok "Yes, we should."
             submitter "boss,DK"
             parameters {
                 string(name: 'PERSON', defaultValue: 'Mr Manoj', description: 'Who should I say hello to?')
             }
        }
        steps {
            sh 'echo ENV_URL=${ENV_URL}'
        }
    }
    stage('When Example') {
        when {
            branch 'main'
        }
        steps {
            echo 'Deploying'
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




