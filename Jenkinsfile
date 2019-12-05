pipeline {
    agent any
    stages {
        stage('build Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.3.9' ){
                sh 'mvn clean compile'
                }
            }
        }
		
		stage('Testing Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.3.9' ){
                sh 'mvn test'
                }
            }
        }
		
		stage('Deploy Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.3.9' ){
                sh 'mvn deploy'
                }
            }
        }
    }
}