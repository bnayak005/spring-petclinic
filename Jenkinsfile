pipeline {
  agent any
  stages {
    stage('Initialization') {
      steps {
        echo 'echo \'Execution started!!!\''
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