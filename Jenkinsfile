pipeline {
   agent any
   stages {
      stage('Say Hello') {
        steps {
            echo 'Hello World!'   
            sh 'java -version'
        }
      }
      stage('Deploy') {
      input {
        message "Should we continue?"
      }
      steps {
        echo "Continuing with deployment"
      }
      stage('Checkpoint') {
         agent none
         steps {
            checkpoint 'Checkpoint'
         }
      }
    }
  }
}
 

