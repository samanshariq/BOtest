pipeline {
  agent any
  stages {
    stage('print') {
      parallel {
        stage('print') {
          steps {
            echo 'Hello World'
          }
        }
        stage('2nd print') {
          steps {
            sh '''echo \'Hello London\'
'''
          }
        }
      }
    }
  }
}