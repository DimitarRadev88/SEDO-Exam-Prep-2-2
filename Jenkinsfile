pipeline {
    
    agent any

    stages {
        stage("Checkout repo") {
            steps {
                checkout scm
            }
        }

        stage("Restore Dependencies") {
            steps {
                bat 'dotnet restore'
            }
        }

        stage("Build Project") {
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage("Test Project") {
            steps {
                bat 'dotnet test'
            }
        }
        
    }

}