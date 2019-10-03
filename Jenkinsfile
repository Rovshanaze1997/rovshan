pipeline {
  agent { label 'linux' }
  tools {
    maven
  }
  stages {
    stage('checkout') {
      steps {
        git 'https://github.com/Rovshanaze1997/rovshan.git'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }
    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }
  }
}
