pipeline {
    agent any

    tools {
        maven 'Maven' // Name of Maven installation in Jenkins
        jdk 'JDK8' // Name of JDK installation in Jenkins
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

