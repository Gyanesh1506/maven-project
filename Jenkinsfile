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
        stage ('Building pkg') {
            steps {
              withMaven(maven: 'MAVEN_HOME') {
              sh 'mvn test'
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

