pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo "hello world is building"'
            
          },
          "Code Quality": {
            sh '''echo "Checking Quality of Hello World"
sleep 20s'''
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        sh 'echo "You must test what you built"'
      }
    }
    stage('Stage') {
      steps {
        sh 'echo "Make sense to "'
        input(message: 'Press to continue', id: 'press', ok: 'yes')
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deplyoed finally"'
      }
    }
  }
}