flag = false
pipeline {
  agent any
  parameters {
      string(name: 'VERSION',defaultValue:'',description:'version to deploy on prod')
      choice(name: 'VERSION',choices:['1.1.0','1.2.0','1.3.0'],description:'')
      booleanParam(name:'executesTests',defaultValue: true, description:'')
    }
  environment {
    NEW_VERSION = '1.3.0'
  }
  stages {
    stage('Build') {
      steps {
         echo 'Building..'
        // Here you can define commands for your
        echo "building version ${New_VERSION}"
      }
    }
    stage('Test') {
      when {
        expression {
          params.executeTests
        }
      }
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
      echo 'Always run this step'
    }
    failure {
      echo 'Failed, but run this step'
    }
  }
}
