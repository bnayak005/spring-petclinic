pipeline {
  agent any
  stages {
    stage('environment setup') {
      steps {
        bat 'env.PATH = "D:/apache-maven-3.5.0-bin/apache-maven-3.5.0/bin;C:\\\\Windows\\\\System32"'
      }
    }

    stage('checkout') {
      steps {
        git(url: '\'https://github.com/bnayak005/spring-petclinic.git\'', branch: 'master')
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts 'target/*.jar'
      }
    }

    stage('publish junit result') {
      steps {
        junit 'target/surefire-reports/*.xml'
      }
    }

  }
}