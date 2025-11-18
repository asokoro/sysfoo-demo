pipeline{
    agent any

    Tools {
        maven 'Maven 3.6.3'
        jdk 'OpenJDK 11'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                mvn compile
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                mvn clean test
            }
        }
        stage('Package') {
            steps {
                echo 'Deploying...'
                mvn package -DskipTests
            }
        }
    }
}