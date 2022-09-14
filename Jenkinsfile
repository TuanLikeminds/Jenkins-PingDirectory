{
    node('Docker-Jenkins-Pod') {
        stage('Get latest version of code') {
          checkout scm
        }
        stage('Check running containers') {
            container('docker') {  
                sh 'hostname'
                sh 'hostname -i' 
                sh 'docker ps'
                sh 'ls'
            }
            container('kubectl') { 
                sh 'kubectl get pods -n default'
            }
            container('helm') { 
                sh 'helm init --client-only --skip-refresh'
                sh 'helm repo update'
                sh 'helm list -a'
            }
        }         
    }
}