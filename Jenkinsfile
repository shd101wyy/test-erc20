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
                 echo 'Hello from shd101wyy/test-erc20'
                 echo 'websiteOrigin: ' + env.websiteOrigin
                 echo 'bytecodeId:    ' + env.bytecodeId
              }
          }
        }
    }
}