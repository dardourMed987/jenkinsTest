pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Récupérer le code source depuis le référentiel Git
                git 'https://github.com/dardourMed987/jenkinsTest.git'
            }
        }
        
        stage('Build') {
            steps {
                // Utiliser Apache Maven pour construire l'application
                sh 'mvn clean package'
            }
        }
        
        stage('Run') {
            steps {
                // Exécuter l'application Spring Boot
                sh 'java -jar target/appSpringBootJenkins.jar'
            }
        }
        
        stage('Test') {
            steps {
                // Exécuter les tests unitaires
                sh 'mvn test'
            }
        }
    }
}
