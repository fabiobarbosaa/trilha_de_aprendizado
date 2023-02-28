pipeline {
  agent any
}


/* pipeline {
    agent any

    stages{
        stage('Build Image - Jenkins'){
            steps{ 
                script{
                    dockerapp_jenkins = docker.build("elogroup2007/jenkins:0.1.${env.BUILD_ID}-dev", '-f ./jenkins/Dockerfile ./jenkins')
                }
            }
        }
        stage('Http Request - Jenkins') {
            steps {
                script{
                    def response = httpRequest responseHandle: 'STRING',
                           url: 'http://10.2.3.239:8084',
                           validResponseCodes: '200'
                }
            }
        }
        stage('Push Image - Jenkins'){
            steps{ 
                script{
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub_elo'){
                        dockerapp_jenkins.push("0.1.${env.BUILD_ID}-dev")
                        dockerapp_jenkins.push('latest')
                    }
                }
            }
        }
    }
} */
