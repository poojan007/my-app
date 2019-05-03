pipeline {
    agent any
    stages {
        stage('clean') {
            steps {
               // get the mvn home path
               def mvnHome = tool name: 'maven-3', type: 'maven'
               sh "${mvnHome}/bin/mvn clean"
            }
        }
        stage('test') {
            steps {
               // get the mvn home path
               def mvnHome = tool name: 'maven-3', type: 'maven'
               sh "${mvnHome}/bin/mvn test"
            }
        }
        stage('package') {
            steps {
               // get the mvn home path
               def mvnHome = tool name: 'maven-3', type: 'maven'
               sh "${mvnHome}/bin/mvn package"
            }
        }
    }
}
