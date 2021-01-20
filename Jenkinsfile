pipeline {
    agent any
    options { ansiColor('xterm') }
    environment {}
    stages {
        stage('Init title') {
            when { changeRequest() }
            steps { script { currentBuild.displayName = "PR ${env.CHANGE_ID}: ${env.CHANGE_TITLE}" } }
        }
        stage('Checkout') {
            steps {
                script {
                    echo 'Hello from shd101wyy/test-erc20'
                    echo 'websiteOrigin: ' + env.websiteOrigin
                    echo 'bytecodeId:    ' + env.bytecodeId
                }
            }
        }
        stage('Build and Test') {
            stages {
                stage('UI Task') {
                    steps {
                        sh "echo shell ${env.websiteOrigin} ${env.bytecodeId}"
                    }
                }
                // stage('Build Haskell')  { steps { sh 'make build-symbolic-haskell -j4  RELEASE=true' } }
                // stage('UI Task')        { steps { sh ''' make test-ui-task-jenkins TASK_ID=23e088b8-0a1a-498b-b4c8-e613c308acf7 ''' } }
            }
        }
    }
}
