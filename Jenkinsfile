pipeline {
  agent any
  stages {
    stage('stage one') {
      steps {
        echo 'step one'
        sh 'echo \'catenate\' | sudo -S /home/tibco/tibco/tra/5.10/bin/AppManage'
      }
    }
    stage('stage two') {
      steps {
        parallel(
          "stage two": {
            echo 'step two'
            sh 'ls'
            
          },
          "stage three": {
            echo 'step three'
            sh 'pwd'
            
          }
        )
      }
    }
  }
}