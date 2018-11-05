pipeline {
    agent any
        
    stages {
        stage('Compile Stage') {
           
            steps {
                withMaven(Maven : 'maven-3.5.4') {
                sh 'mvn clean compile'
                }
            }
        }
        stage('Test') {
            steps {
                withMaven(Maven : 'maven-3.5.4'){
                sh 'mvn test'
                }
                
            }

           }

        stage('Deploy') {
            steps {
                withMaven(Maven : 'maven-3.5.4') {
                sh 'mvn deploy'
                }
            }
        }
    }
}
