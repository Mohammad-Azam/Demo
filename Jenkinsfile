pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello'
        echo 'Hello2'
        timestamps() {
          echo 'hello3'
        }

      }
    }

    stage('Test') {
      steps {
        mail(subject: 'Jenkins Pipeline ', body: 'Hi, this is testing Blue ocean Pipeline', from: 'inform2me117@gmail.com', to: 'mohazam77229@gmail.com')
        fileExists 'jenkinsfile'
        echo 'jenkins found '
      }
    }

  }
}