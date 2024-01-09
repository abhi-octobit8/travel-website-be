pipeline {
    agent any
    
    
    environment {
        MAVEN_HOME = tool 'Maven'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'GIthubAccess', url: 'https://github.com/abhi-octobit8/ecomm-website-be.git']])
            }
        }
        stage('mvn package') {
            steps {
                sh "${MAVEN_HOME}/bin/mvn package"
            }
        }
    }
    
}
