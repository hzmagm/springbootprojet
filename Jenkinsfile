pipeline {
    agent any
 
 tools{
     maven 'apache-maven-3.6.0'
 }

    stages {
        stage('Git Checkout') {
            steps {
               git credentialsId: 'git_credentials', url: 'https://github.com/hzmagm/springbootprojet.git'
            }
        }
        
        stage('build Maven') {
            steps {
               sh 'mvn compile'
            }
        }
        
        
        
          stage('Test Unitaire') {
            steps {
         
               sh 'mvn clean test'
            
            }
        }
        
          stage('App Package') {
            steps {
     
               sh 'mvn clean package'
           
            }
        }
        
          
    }
}
