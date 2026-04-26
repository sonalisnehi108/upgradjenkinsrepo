pipeline {
    agent any

    stages {
        stage('Install  maven') {
            steps {
               sh 'sudo apt  install maven -y'
            }
        }
         stage('Install jdk') {
            steps {
               sh 'sudo apt install openjdk-21-jdk  -y'
            }
        }

          stage('clone reposiotry') {
            steps {
           git 'https://github.com/hellokaton/java11-examples.git'
            }
        }
        stage('creating package') {
            steps {
           sh 'mvn clean package'
            }
        }
        stage('Release/Achriving Artifact') {
            steps {
           archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
        }
    }
}
