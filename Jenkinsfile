@Library('Shared-lib')_

pipeline{
    agent {label 'dev-server'}

    stages{
        stage("Code Clone"){
            steps{
                clone("https://github.com/vaghelajash/Springboot-BankApp.git","Devops")
                echo "Code clone ho gyaaaaaa!!!!"
            }
        }
        stage("Build"){                                                             
            steps{
                dockerbuild("SpringBoot Bankapp","latest")
                echo "Code build ho gyaaaaaaa!!!"
            }
        }
        stage("Push to DockerHub"){
            steps{
                dockerpush("dockerHub","SpringBoot Bankapp","latest")
                echo "Push to dockerHub ho gyaaaaa!!!"
            }
        }
        stage("Deployment"){
            steps{
                deploy()
                echo "yahhhh Deployment ho gyaaaaa!!!!"
            }
        }
    }
}
