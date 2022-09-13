pipeline { 
    agent any 
    stages {
        stage('Download Docker image') { 
            steps { 
                sh "echo 'building..'"
            }
        }
        stage('Test'){
            steps {
                sh "echo 'Testing...'" 
            }
        }
        stage('Deploy') {
            steps {
                sh "echo 'Deploying the helm charts!!!!! yayyyy"
            }
        }
    }
}