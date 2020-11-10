pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Clone repository..'
                git url: 'https://github.com/suhvas/Pipeline-Maven.git'
            }
        }
        stage('Building') {
            steps {
                echo 'Building..'
                def mvnHome = tool 'M3'
                sh "${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
