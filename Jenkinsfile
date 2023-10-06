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

        stage('Test3') {
          steps {
            echo "This is test3 for environment variable : ${PresentationPath}"
          }
        }

      }
    }

    stage('Deploy') {
      when {
        branch 'master'
      }
      parallel {
        stage('Deploy') {
          steps {
            input 'Do you want to deploy?'
            echo 'Deployed the changes'
          }
        }

        stage('Artifacts') {
          steps {
            writeFile(file: 'testFile.txt', text: 'Hello World!')
          }
        }

      }
    }

  }
  environment {
    PresentationPath = 'D:\\Personal\\certificate\\presentations'
  }
}