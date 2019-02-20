pipeline {
  agent any
  stages {
    stage('print') {
      parallel {
        stage('print') {
          steps {
            sh 'echo \'building project\''
          }
        }
        stage('') {
          steps {
            sh '''echo \'Hello World\'
'''
          }
        }
      }
    }
    stage('Run a program') {
      steps {
        echo 'Hello world'
      }
    }
  }
}