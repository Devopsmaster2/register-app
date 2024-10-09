Pipeline {
  agent {label 'Jenkins-Agent'}
  tools {
    jdk 'Java21'
    maven 'Maven3'   
  }
  stages{
    stage("Cleanup Workspace"){
      steps{
        cleanWs()
      }
    }
    stage("Chekout from SCM"){
      steps{
        git branch: 'main' , credentialsId: 'github' , url: 'https://github.com/Devopsmaster2/register-app'
      }
    }

    stage

    
  }
}
