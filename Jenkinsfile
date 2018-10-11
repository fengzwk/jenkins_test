pipeline {
    agent any
    checkout scm	
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -Dmaven.test.skip=true'
            }
        }
    }
}
