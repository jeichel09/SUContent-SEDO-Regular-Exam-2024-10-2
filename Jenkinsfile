pipeline{
  agent any

  stages {
      stage('Restore dependencies') {
        steps {
          bat 'dotnet restore'
        }
      }
      stage('Dotnet build') {
        steps {
          bat 'dotnet build --configuration Release'
        }
      }
      stage('Execute tests') {
        steps {
          bat 'dotnet test --configuration Release --no-build --verbosity normal'
        }
      }
  }
}
