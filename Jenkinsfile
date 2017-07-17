pipeline {
  agent any
  stages {
    stage('stage one') {
      steps {
        echo 'step one'
      }
    }
    stage('step two') {
      steps {
        parallel(
          "stage two": {
            echo 'step two'
            
          },
          "stage three": {
            echo 'step three'
            
          }
        )
      }
    }
  }
}