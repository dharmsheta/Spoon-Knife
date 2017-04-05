pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        sh 'echo "hello prep"'
        sh 'sleep 10s'
      }
    }
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo "building a SW"'
            
          },
          "Code Coverage": {
            sh 'echo "code quality check"'
            
          }
        )
      }
    }
    stage('Finish') {
      steps {
        sh 'echo "we\'re done"'
      }
    }
  }
}