pipeline {
  agent any
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
            emailext(attachLog: true, body: '''Hi Koder,

                                                    This is for the jenkins email notification 

                                                    Regards,
                                                    Jenkins Admin''', compressLog: true, subject: 'Jenkins Extended mail ', to: 'copypaste.koder@gmail.com')
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
