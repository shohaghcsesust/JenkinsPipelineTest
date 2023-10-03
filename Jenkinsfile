pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build the project'
      }
    }

    stage('Test') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Test all the cases'
          }
        }

        stage('Test2') {
          steps {
            echo 'Parallel test'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed the changes'
        input 'Do you want to deploy?'
      }
    }

  }
}