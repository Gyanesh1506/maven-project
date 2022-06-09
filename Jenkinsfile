pipeline {
    agent maven
    stages {
        stage ('Bulding maven code') {
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
