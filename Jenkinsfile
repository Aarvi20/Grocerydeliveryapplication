pipeline {
    agent any
      tools {
        jdk "Java8"
    }
    stages {
        stage('---clean---') {
            steps {
           
                bat "mvn clean"
            }
        }
        stage('---Installing---') {
            steps {
                bat "mvn install"
            }
        }
        stage('--Compiling--') {
            steps {
                bat "mvn compile"
            }
        }
        stage('--package--') {
            steps {
                bat "mvn package"
            }
        }
                stage('--test--') {
            steps {
                bat "mvn test"
            }
        }
          stage("Sonar Qube Analysis") {
            steps {
                bat "mvn verify sonar:sonar"
            }
        }
        
    }
}