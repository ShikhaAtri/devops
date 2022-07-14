pipeline {
    agent any
    tools {
    	maven 'My_Maven'
	}
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'shikha',
		credentialsId: '7245f3ce-de0c-4e3c-a77f-63a08d879a20',
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
