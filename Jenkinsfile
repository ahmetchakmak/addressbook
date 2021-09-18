pipeline{
    agent any
    stages {
        stage('Pull the code') {
            steps{
                git branch:'develop', credentialsId:'Github', url:'https://github.com/ahmetchakmak/addressbook.git'
            }
        }
        stage("Build") {
            steps{
                sh 'mvn compile -B'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test -B'
            }
        }
        stage('package') {
            steps{
                sh 'mvn package -B'
            }
        }
    }
}
