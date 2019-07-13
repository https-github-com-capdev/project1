pipeline {
   agent any
   stages {
      stage('Say Hello') {
         stage('Deploy') {
      input {
        message "Should we continue?"
      }
      steps {
        echo "Continuing with deployment"
      }
    }
         steps {
            echo 'Hello World!'   
            sh 'java -version'
         }
      }
   }
}

