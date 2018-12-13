pipeline {
    agent any

    tools {
        maven 'Maven 3.5.4'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            step {
                echo 'Testing...'
                sh 'mv test'
            }
        }
        stage('Package) {
            step {
                echo 'Packaging...'
                sh 'mv -DskipTests package'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
     }
}
