pipeline {
    agent any

    tools {
        jdk 'JDK21'
        maven 'Maven3'
    }

    stages {
        stage('Recuperation du projet') {
            steps {
                echo 'Recuperation depuis GitHub'
                checkout scm
            }
        }

        stage('Generation du livrable') {
            steps {
                dir('backend') {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }
    }
}