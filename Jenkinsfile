pipeline {
    agent any

    stages {
        stage ('compilation stage') {

            steps { 
                withMaven(maven : 'maven3.8.5') {
                    sh 'mvn clean compile'
                }
            }
        }
       
        stage ('Testing stage') {
            steps { 
                withMaven(maven : 'maven3.8.5') {
                    sh 'mvn test'
                }
            }          
        }
      
            stage ('Deployement stage') {
            steps { 
                withMaven(maven : 'maven3.8.5') {
                    sh 'mvn deploy'
                }
            }          
        }
    }
}
