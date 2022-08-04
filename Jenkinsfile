pipeline {
    agent any
    tools {
        maven "MAVEN"
    }
    
    stages {
        
        stage('Build Maven') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'patilashishp', url: 'https://github.com/patilashishp/jenkins-nexus.git']]]
