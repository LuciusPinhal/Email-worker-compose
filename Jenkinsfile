pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                dir("Teste"){
                    bat ' docker container run -d'
                  
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