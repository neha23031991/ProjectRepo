pipeline {
  agent any 
  environment {

    
  }

  stages 
  {
      stage('checkout')
      steps 
      {
         checkout scm
      }
      stage('Build') {
            steps {
                sh 'echo "Starting build..."'
                sh 'make build'
                sh 'echo "Build complete."'
            }
        }

     stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                sh './jenkins/scripts/test.sh'
                sh 'echo "Tests passed."'
            }
        }

      stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                sh 'echo "Deploying to production..."'
            }
        }
    }
}
