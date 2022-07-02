pipeline {
    agent any
    stages {  
        stage ('Testing maven code') {
            steps {
                withMaven(maven: 'MAVEN_HOME') {
                sh 'mvn test'
                }
            }
        } 
        stage ('Sonar') {
            steps {
                withMaven(maven: 'MAVEN_HOME') {
                   withSonarQubeEnv(credentialsId: 'Sonar', installationName: 'sonar') {
                   sh 'mvn package sonar:sonar'
                  }
                }    
            }
        }     
        stage ('Printing status') {
            steps {
                echo 'This is successful'
            }
        }     
    }
}

