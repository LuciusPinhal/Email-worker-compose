pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                dir("Teste"){
                    bat ' docker container run -d --name comdockercompose --net host alpine sleep 1000'
                   bat ' docker container run -d --name comdockercompose-frontend-1 --net host alpine sleep 1000'
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


        
    }
}