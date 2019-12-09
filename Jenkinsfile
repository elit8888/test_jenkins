pipeline {
  agent {
    node {
      label 'dlp'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'printenv'
      }
    }

    stage('Test') {
      parallel {
        stage('Platform A') {
          steps {
            echo 'Testing'
          }
        }

        stage('Platform B') {
          steps {
            echo 'Test 2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
        dir(path: 'output') {
          pwd()
        }

      }
    }

  }
}