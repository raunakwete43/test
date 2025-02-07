pipeline {
  agent any

  triggers {
    cron('* * * * *')
  }

  stages {
    stage('Checkout') {
      steps {
        script{
          git url: 'https://github.com/raunakwete43/test.git', branch: 'main'
        }
      }
    }
    stage('Java Build') {
      steps {
        echo 'Building java app'
        sh 'javac main.java'
      }
    }
    stage('Java Execute') {
      steps {
        echo 'Running main.java'
        sh 'java main'
      }
    }
    stage('Python Execute') {
      steps {
        echo 'Running Python program'
        sh 'python test.py'
      }
    }
  }
}
