pipeline {
    agent any
    tools {
    	maven 'My_Maven'
	}
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main',
		credentialsId: '6c504807-6762-46a9-a176-5693cb4c3c2c',
		url: 'https://github.com/cloudtechner/testrepo.git'
            }
        }    
        stage('Compile') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Unit Test') {
            steps {
                sh 'mvn test'
            }
        }
	stage('Deploy To Environment') {
            steps {
                sh 'echo Deployment Done'
            }
        }
    }
}
