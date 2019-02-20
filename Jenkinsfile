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
    stage('run') {
      steps {
        writeFile(file: 'flask app.py', text: 'Flask', encoding: 'from flask import Flask app = Flask(__name__)  @app.route(\'/\') @app.route("/home") def home():     return \'<h1>Hello, World!</h1>\'  if __name__ == \'__main__\':     app.run(debug=True)')
      }
    }
  }
}