pipeline 
{
  agent any
  parameters {
  //these are types of parameters
  string(name: 'VERSION', defaultValue: '', description: 'version to deploy on prod') 
  choice (name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '') 
  booleanParam(name: 'executeTests', defaultValue: true, description: '')
  }
  environment
  {
    "NEW_VERSION = '1.3.0'
  }
  stages 
  {
    stage('Build') 
    {
      steps 
      {
        echo 'Building..'
        // Here you can define commands for your build
        echo 'Building Version &(NEW_VERSION)'
      }
    }
    stage('Test') 
    {
      steps 
      {
        echo 'Testing..'
        // Here you can define commands for your tests
      }
    }
    stage('Deploy') 
    {  
      steps 
      {
        echo 'Deploying....'
        // Here you can define commands for your deployment
      }
    }
  }
  post
  {
    //conditions here will be executed after build
    always
    {
      //always run despite build failed
      echo "Post build condition running'
      failure
      {
        //only if build is failed
        echo 'Post action if build failed
      }
    }
  } 
}
