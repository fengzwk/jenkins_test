pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }	
    stages {
        stage('Build') {
            steps {
		checkout scm
                sh 'mvn clean package -Dmaven.test.skip=true'
            }
        }
    }
    post{
	always{
		echo 'develop build successfully!!'
	}
    }	
}
