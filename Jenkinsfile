pipeline {
    agent any

    environment {
        JAVA_HOME = 'C:\Program Files\Java\jdk-21'  // Update this with your path
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Sonalip-22/demo-ci-cd.git'  // Change to your repo
            }
        }

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
}
