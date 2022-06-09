pipeline {
    agent any
    stages {
        stage ('Pulling code from Git') {
            steps {
                git branch: 'master', url: 'https://github.com/Gyanesh1506/maven-project.git'
            }
        }
        stage ('Bulding maven code') {
            steps {
                withMaven(maven: 'MAVEN_HOME') {
                sh 'mvn test'
                }
            }
        }        
    }
}
