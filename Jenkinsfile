pipeline {
    agent any
    stages {
        stage ('Build Compose') {
            dir("Teste"){
                    bat 'docker compose up -d'
                
                }                
            }
        }
        stage ('Test Image') {
            steps {
                dir("Teste"){
                    bat 'docker image ls'
                    echo 'Teste realizado com sucesso'
                }
            }
        }
        // stage ('simple-tag') {
        //     steps {
        //         dir("tag"){
        //             bat 'docker image tag api-produto:49 lucius28/api-produto'
        //             echo 'Tag Realizada com sucesso'

        //             bat 'docker image push lucius28/api-produto'
        //             echo 'Push Realizada com sucesso'
                
        //         }
        //     }
        // }


        stage ('Push Image no docker Hub') {
            steps {
                script {
                    //criar credencial ou token de acesso
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        dockerapp.push('latest')
                        dockerapp.push("${env.BUILD_ID}")
                    }
                }
            }
        }
    }
}