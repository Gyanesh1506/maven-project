pipeline {
    agent any
    stages {
        stage ('Bulding maven code') {
            steps {
                withMaven(maven: 'MAVEN_HOME') {
                sh 'mvn test'
                }
            }
        }        
    }
}
