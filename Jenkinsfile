pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        sh 'mvn compile'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
        sh 'mvn clean test'
      }
    }

    stage('Package') {
      steps {
        echo 'Deploying...'
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.9.11'
  }
}