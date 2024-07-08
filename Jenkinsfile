pipeline {
  agent any
  stages {
    stage('unit-test') {
      steps {
        sh 'echo "This is a test"'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'Build'
          }
        }

        stage('error') {
          steps {
            sleep 10
            sh 'pwd'
          }
        }

      }
    }

    stage('push') {
      steps {
        sh 'echo "Push image"'
      }
    }

  }
}