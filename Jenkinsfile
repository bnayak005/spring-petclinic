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
        echo 'echo \'checking out the code!!!\''
      }
    }

    stage('build') {
      steps {
        echo 'echo \'building out the code!!!\''
      }
    }

    stage('Unit Test') {
      parallel {
        stage('Unit Test') {
          steps {
            echo 'echo \'It\'s Unit test!!!\''
          }
        }

        stage('Api Test') {
          steps {
            echo 'echo \'It\'s Api test!!!\''
          }
        }

        stage('Db Test') {
          steps {
            echo 'echo \'It\'s Db Test!!!\''
          }
        }

      }
    }

    stage('publish') {
      steps {
        echo 'echo \'publishing result!!!\''
      }
    }

  }
}