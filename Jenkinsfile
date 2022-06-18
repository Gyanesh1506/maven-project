pipeline {
    agent any
    stages {
        stge ('Pulling code from Git') {
            steps {
                git branch: 'gyanesh', url: 'https://github.com/Gyanesh1506/maven-project.git'
            }
        }    
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

