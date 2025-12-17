pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                echo 'Compilation du projet Java...'
                sh '''
                mkdir -p out
                javac -d out src/org/example/jenkins/tp2.java
                '''
            }
        }

        stage('Run') {
            steps {
                echo 'Execution du programme Java...'
                sh '''
                java -cp out org.example.jenkins.tp2
                '''
            }
        }
    }
}
