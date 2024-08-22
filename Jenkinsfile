pipeline {
    agent any
    tools {nodejs "NodeJS"}
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Test') { 
            steps {
                sh "chmod +x -R ${env.WORKSPACE}"
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}