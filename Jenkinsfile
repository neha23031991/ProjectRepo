pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Change 'sh' to 'bat' for Windows batch commands
                bat 'echo "Starting build..."'
                // Replace 'make build' with a valid Windows build command
                // Example for Maven on Windows:
               
                bat 'echo "Build complete."'
            }
        }

        stage('Test') {
            steps {
                // Similarly, change 'sh' to 'bat' for your test command
                bat 'echo "Running tests..."'
                // Example for a .NET test command on Windows:
                // bat 'dotnet test'
                bat 'echo "Tests passed."'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                bat 'echo "Deploying to production..."'
                // Add your Windows-based deployment commands here.
            }
        }
    }
}
