pipeline {
    agent any
    tools {
        docker 'docker'
    }
    stages {
        stage("init") {
            steps {
                script {
                    echo "hello"
                }
            }
        }
        stage("build jar") {
            steps {
                script {
                    //sh 'dotnet clean'
                    //sh 'dotnet publish -c Release'
                    sh 'docker --version'
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    //sh 'docker build -t dockerdemo .'
                    //gv.buildImage()
                    echo "hi"
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    //sh 'docker run -d -p 8081:80 --name myapp dockerdemo'
                    echo "hi"
                }
            }
        }
    }   
}