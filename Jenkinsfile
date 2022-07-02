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
                withSonarQubeEnv(credentialsId: 'Sonar') {
                sh 'mvn package sonar:sonar'
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

