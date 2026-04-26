pipeline {
    agent any

    tools {
        maven 'maven3'
    }

    stages {
        stage('CHECKOUT') {
            steps {
                git 'https://github.com/Srushti-hidakal/c1.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}