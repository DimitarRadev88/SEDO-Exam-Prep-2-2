pipeline {

    stages {
        stage("Checkout repo") {
            step {
                checkout scm
            }
        }

        stage("Restore Dependencies") {
            step {
                bat 'dotnet restore'
            }
        }

        stage("Build Project") {
            step {
                bat 'dotnet build --no-restore'
            }
        }

        stage("Test Project") {
            step {
                bat 'dotnet test'
            }
        }
        
    }

}