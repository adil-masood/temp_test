pipeline {
    agent any
    stages {
        stage('Build')
        {
            steps 
            {
                script{
                    python temp.py
                    echo "Hello Jenkins"
                }
            }
        }
    }
    post {
        always{
            echo "Always"
        }
        success{
            echo "Success"
        }
        failure{
            echo "Failure"
        }
  }
    
}
