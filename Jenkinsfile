pipeline {
    agent any
    tools {
        maven 'localMaven'
        jdk 'localJDK'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
                bat 'docker build . -t tomcatwebapp:latest'
            }
        }
    }
}
