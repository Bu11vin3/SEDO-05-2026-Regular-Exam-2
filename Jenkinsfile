pipeline{
    agent any 
    stages{

        stage('Dotnet Restore'){
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps{
                sh "dotnet restore"
            }
        }
        stage('Dotnet Build'){
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps{
                sh "dotnet build --no-restore"
            }
        }
        stage('Dotnet Test'){
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps{
                sh "dotnet test --no-build --verbosity normal"
            }
        }
    }
}