pipeline {
    agent any
    tools {
        maven "Maven"
    }
    
    stages {
        
        stage('Build Maven') {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '281de1f4-2941-41a1-b6bc-9c0865e2e111', url: 'https://github.com/patilashishp/jenkins-nexus.git']]])
                
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
                
            }    
        }
    }
}   
