pipeline {
    agent any
    stages {
        stage('build Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.3.9' ){
                sh 'mvn -B -DskipTests clean compile'
                }
            }
        }
		
		stage('Testing Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.3.9' ){
                sh 'mvn -B -DskipTests test'
                }
            }
        }
		
		stage('Deploy Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.3.9' ){
                sh 'mvn -B -DskipTests deploy'
                }
            }
        }
    }
}