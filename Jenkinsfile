pipeline {
    agent node("myAgent")
    stages {
        stage('Ping_Deploy') {
            steps {
                sh "sudo -S cp /home/appuser/.kube/config ~jenkins/.kube/"
                sh "sudo chown -R jenkins: ~jenkins/.kube/"
                sh "sudo -S cp -r /home/appuser/.aws ~jenkins/.aws/"
                sh "sudo chown -R jenkins: ~jenkins/.aws/"
                sh "kubectl get po"
                sh "git init"
                sh "git clone https://github.com/ganesh-idm/pipeline.git ./manifest"
                sh "kubectl apply -f ./manifest/pipeline_manifest.yml -n us-east-1"
                sh "rm -rf manifest"
                sh "sleep 300"
                sh "kubectl get po"
                }
        }
    }
}