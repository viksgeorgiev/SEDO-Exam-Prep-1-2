pipeline {
    agent any

    when {
        anyOf {
            branch "main"
            branch "feature/*"
        }
    }

    stages {
        stage("Restore the app") {
            steps {
                bat "dotnet restore"
            }
        }

        stage("Build the app") {
            steps {
                bat "dotnet build"
            }
        }

        stage("Test the app") {
            steps {
                bat "dotnet test"
            }
        }
    }
}