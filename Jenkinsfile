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
    stage('Time limit') {
      steps {
        timeout(time: 5, activity: true)
      }
    }
    stage('retry') {
      steps {
        retry(count: 10)
      }
    }
    stage('Archives') {
      steps {
        archiveArtifacts(artifacts: 'BOtest', caseSensitive: true)
      }
    }
  }
}