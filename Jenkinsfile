pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		checkout scm
                sh 'mvn clean package -Dmaven.test.skip=true'
            }
        }
    }
}
