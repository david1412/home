pipeline {
    agent any
        
    
    stages {
        stage('Compile Stage') {
           
            steps {
                withMaven(Maven : 'Maven') {
                sh 'mvn clean compile'
                }
            }
        }
        stage('Test') {
            steps {
                withMaven(Maven : 'Maven'){
                sh 'mvn test'
                }
                
            }

           }

        stage('Deploy') {
            steps {
                withMaven(Maven : 'Maven') {
                sh 'mvn deploy'
                }
            }
        }
    }
}
