pipeline {
    agent any
    stages {
        stage('Ping_Deploy') {
            steps {
                sh "sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common"
                sh "curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -"
                sh "sudo apt-key fingerprint 0EBFCD88"
                sh "sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu  $(lsb_release -cs) stable" "
                sh "sudo apt-get update"
                sh "sudo apt-get install -y docker-ce"
                sh "sudo groupadd docker"
                sh "sudo usermod -aG docker $USER"
                sh "sudo systemctl enable docker"
                }
        }
    }
}
