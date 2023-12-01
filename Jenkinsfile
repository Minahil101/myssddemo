pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        // Here you can define commands for your build
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      // Here you can define commands for your tests
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      // Here you can define commands for your deployment
      }
    }
 
  }
  post {
    // the conditions after build
    always {
      echo 'will run always'
    }
    failure {
      echo 'failed condition'
    }
    success {
      echo 'success condition'
    }
  }
}
