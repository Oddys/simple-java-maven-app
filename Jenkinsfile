pipeline {
    agent {
        docker {
            image 'maven:3-jdk-8'
            args '-v C:/Users/Yurii_Honcharenko1/.m2:/root/.m2'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
