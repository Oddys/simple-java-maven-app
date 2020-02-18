pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-u 0 --dns 10.17.110.3'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'whoami'
                sh 'mvn --version'
                sh 'cat /etc/resolv.conf'
                sh 'ping -c 1 8.8.8.8'
                sh 'ping -c 1 216.58.209.14'
                sh 'ping -c 1 repo.maven.apache.org'
                sh 'mvn -X clean compile'
            }
        }
    }
}
