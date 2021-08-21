pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/sasha-by/cats.git', branch: 'main', credentialsId: '4c6eb882-1250-4039-b94e-9f54f9b86157', poll: true)
      }
    }

    stage('build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy to dev 1') {
      parallel {
        stage('Deploy to dev 1') {
          steps {
            sleep 30
            echo 'finished'
          }
        }

        stage('Deploy to dev 2') {
          steps {
            sleep 50
            echo 'completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing'
      }
    }

  }
}