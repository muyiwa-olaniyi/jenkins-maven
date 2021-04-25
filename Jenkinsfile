pipeline {
    agent any 
    stages {
        stage('Compile and Clean') { 
            steps {
                
                sh "mvn clean compile"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package"
            }
        }
        stage('Achiving') { 
            steps {
                sh "archiveArtifacts '**/target/*.jar'"
            }
        }
    }
}
