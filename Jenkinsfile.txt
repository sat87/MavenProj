pipeline {
    agent any 
    stages {
        stage('Clone') { 
            steps {
                
                bat "mvn clean"
            }
        }
        stage('Test') { 
            steps {
                bat "mvn test" 
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package" 
            }
        }
    }
}