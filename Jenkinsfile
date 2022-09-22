pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/mabedd/YouTube-React-Clone-MUI', branch: 'main')
      }
    }

    stage('logs') {
      parallel {
        stage('error') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Deps') {
          steps {
            sh 'npm i'
          }
        }

      }
    }

  }
}