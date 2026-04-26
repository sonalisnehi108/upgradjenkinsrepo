pipeline {
    agent any

    stages {
        stage('Install maven') {
            steps {
               sh 'sudo apt  install maven -y'
            }
        }
         stage('Install jdk') {
            steps {
               sh 'sudo apt install openjdk-21-jdk  -y'
            }
        }

        stage('Clone repo') {
            steps {
               git branch: 'main', url: 'https://github.com/hellokaton/java11-examples.git'
            }
        }
    }
}
