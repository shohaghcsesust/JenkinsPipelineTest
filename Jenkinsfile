pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build1') {
          steps {
            echo 'Build the project'
          }
        }

        stage('Build2') {
          steps {
            echo 'Parallely build'
          }
        }

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
      parallel {
        stage('Deploy1') {
          steps {
            echo 'Deployed the changes'
          }
        }

        stage('Deploy2') {
          steps {
            echo 'Parallel deployment'
          }
        }

      }
    }

  }
}