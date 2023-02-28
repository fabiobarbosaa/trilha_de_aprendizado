pipeline {
    agent any

    stages{
        stage('Build Image'){
            steps{ 
                script{
                    dockerapp = docker.build("fabiobarbosaa/ci_cd:0.1.${env.BUILD_ID}-dev", '-f ./src/Dockerfile ./src')
                }
            }
        /* }
        stage('Http Request') {
            steps {
                script{
                    def response = httpRequest responseHandle: 'STRING',
                           url: 'http://localhost:8080/',
                           validResponseCodes: '200'
                }
            }
        }
        stage('Push Image'){
            steps{ 
                script{
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub'){
                        dockerapp.push("0.1.${env.BUILD_ID}-dev")
                        dockerapp.push('latest')
                    }
                }
            }
        } */
    }
}

        // stage('Checkout Release') {
        //     steps {
        //        checkout([$class: 'GitSCM', branches: [[name: 'release']], extensions: [], userRemoteConfigs: [[credentialsId: 'dev', url: 'https://dev.azure.com/eloanalytics/_git/SEFAZ-PI%20Big%20Data%20Analytics%20Pauta%20Fiscal']]])
        //     }
        // }
        // stage('Criação de Release') {
        //     steps {
        //        sh 'test -f release.tar.gz && rm release.tar.gz && tar -czvf release.tar.gz * || tar -czvf release.tar.gz *'
        //     }
        // }
        // stage('Deploy') {
        //     steps {
        //         sshPublisher(publishers: [sshPublisherDesc(configName: 'prod', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'tar -xzvf release.tar.gz', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'release.tar.gz')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
        //     }
        // }    
        //} 
}
