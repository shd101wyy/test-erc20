pipeline {
    agent any
    environment {
        IS_AUTO_TRIGGERED = false;
        userInput = null;
        target_dir= null;
    }
    stages {
        stage('Checkout') {
           steps {
              script {
                 echo 'websiteOrigin: ' + env.websiteOrigin
                 echo 'bytecodeId:    ' + env.bytecodeId
              }
          }
        }
    }
}