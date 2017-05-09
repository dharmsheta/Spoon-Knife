pipeline {
  agent any
  stages {
    stage('Commit') {
      steps {
        parallel(
          "Commit": {
            sh 'echo "source code checked out"'
            
          },
          "Code Quality": {
            sh 'echo "code quality verified"'
            
          }
        )
      }
    }
    stage('Build') {
      steps {
        sh 'echo "build"'
      }
    }
  }
}