pipeline {
  agent {
    docker {
      image 'ubuntu'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Hello2'
            timestamps() {
              echo 'hello3'
            }

          }
        }

        stage('Build2') {
          steps {
            emailext(subject: 'Jenkins Extended plugin ', body: 'this is for testing email using new plugin ', attachLog: true, from: 'inform2me1137@gmail.com', to: 'mohdazam77229@gmail.com', compressLog: true)
          }
        }

      }
    }

    stage('Test') {
      steps {
        fileExists 'jenkinsfile'
        echo 'jenkins found '
      }
    }

  }
}