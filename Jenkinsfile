pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo "I\'m building"'
            
          },
          "Code Coverage": {
            sh 'echo "Checking code quality"'
            
          },
          "License Check": {
            sh 'echo "Also doing license check"'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        sh 'echo "Let\'s test it"'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Time to deploy"'
      }
    }
  }
}