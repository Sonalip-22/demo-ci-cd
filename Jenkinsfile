pipeline {
    agent any

    environment {
        JAVA_HOME = '/usr/lib/jvm/java-21-openjdk-amd64'
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sonalip-22/demo-ci-cd.git'
            }
        }

        stage('Build') {
            steps {
                // Build without testing
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                // Run tests separately
                sh 'mvn test'
            }
        }
    }
}
