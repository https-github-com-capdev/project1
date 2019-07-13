pipeline {
  agent any
  stages {
    stage('Say Hello') {
      parallel {
        stage('Say Hello') {
          steps {
            echo 'Hello World!'
            sh 'java -version'
          }
        }
        stage('') {
          steps {
            sh '''pipeline {
    agent {
    label \'jdk9\'
  }
   stages {
      stage(\'Say Hello\') {
         steps {
            echo \'Hello World!\'   
            sh \'java -version\'
         }
      }
   }
}'''
            }
          }
        }
      }
      stage('Checkpoint') {
        steps {
          checkpoint 'Checkpoint'
        }
      }
      stage('Deploy') {
        input {
          message 'Should we continue?'
        }
        steps {
          echo 'Continuing with deployment'
        }
      }
    }
  }