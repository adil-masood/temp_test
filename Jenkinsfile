pipeline {
    agent any
    stages {
        stage('Build')
        {
            steps 
            {
                script{
                    bat "python temp.py"
                    echo "Hello Jenkins"
                }
            }
        }
    }
    post {
        always{
            echo "Always"
            slackSend channel: 'personal', color: 'green', message: 'Hello World', teamDomain: 'temptest-headquarters', tokenCredentialId: 'temptest'
        }
        success{
            echo "Success"
            slackSend channel: 'personal', color: 'green', message: 'Success', teamDomain: 'temptest-headquarters', tokenCredentialId: 'temptest'
        }
        failure{
            echo "Failure"
            slackSend channel: 'personal', color: 'green', message: 'Failed', teamDomain: 'temptest-headquarters', tokenCredentialId: 'temptest'
        }
  }
    
}
