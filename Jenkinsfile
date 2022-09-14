pipeline {
    agent any
    stages {
        stage('Ping_Deploy') {
            steps {
                sh "apt-get install -y apt-transport-https ca-certificates curl software-properties-common"
                sh "curl -fsSL https://download.docker.com/linux/ubuntu/gpg |   apt-key add -"
                sh "apt-key fingerprint 0EBFCD88"
                sh "add-apt-repository 'deb [arch=amd64] https://download.docker.com/linux/ubuntu  \$(lsb_release -cs) stable' "
                sh "apt-get update"
                sh "apt-get install -y docker-ce"
                sh "groupadd docker"
                sh "usermod -aG docker $USER"
                sh "systemctl enable docker"
                }
        }
    }
}
