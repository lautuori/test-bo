pipeline {
  agent any
  stages {
    stage('stage one') {
      steps {
        echo 'step one'
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
