pipeline{
    agent any
    stages{
        stage('Build'){
            steps { sh 'mvn clean package' }
        }
    post{
        always{
            archieveArtifacts artifacts: 'target/*.jar',fingerprint:true
        }
    }
}
