pipeline {
    agent any
    stages {
        stage ("InstallMvn") {
            steps {
                sh 'sudo docker inspect -f . maven:3-alpine'
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
