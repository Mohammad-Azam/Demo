pipeline {
  agent {
    docker {
      image 'ubuntu'
    }

  }
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
        mail(subject: 'Jenkins Pipeline ', body: 'Hi, This is testing Blue ocean Pipeline', from: 'inform2me117@gmail.com', to: 'mohdazam77229@gmail.com')
        fileExists 'jenkinsfile'
        echo 'jenkins found '
      }
    }

  }
}