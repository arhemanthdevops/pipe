#
pipeline {
    agent any

    tools {
        maven 'Maven' 
        jdk 'JDK8' 
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution complete!'
        }
    }
}

