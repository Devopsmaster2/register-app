pipeline {
    agent { label 'Jenkins-Agent' }
    tools {
        jdk 'Java21'
        maven 'Maven3'
    }
    
    stages{
        stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
        }

        stage("Checkout from SCM"){
                steps {
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/Devopsmaster2/register-app'
                }
        }

        stage("Build Application") {
            steps {
                sh "mvn -X clean package"
            }
        }

        stage("Test Application") {
            steps {
                sh "mvn -X test"
            }
        }

    }
}
