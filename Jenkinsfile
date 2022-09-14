pipeline {
    
    agent any
    stages {
        stage('Ping_Deploy') {
            steps {
                sh "echo hello from the other side"
                sh "apt-get update"
                sh "apt-get install ca-certificates curl gnupg lsb-release"
                }
        }
    }
}