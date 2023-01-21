pipeline {
    agent any
    stages {
        stage("start") {
            steps {
                script {
                    echo "hello"
                }
            }
        }
        stage("publish file") {
            steps {
                script {
                    sh 'dotnet publish -c Release'
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    sh 'docker build -t dockerdemo .'
                    
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    sh 'docker run -d -p 8081:80 --name myapp dockerdemo'
                    
                }
            }
        }
    }   
}