pipeline{
     agent any
     tools{

         maven 'mymaven'
         jdk 'myjava'
     }
    stages{
        stage('git_checkout'){

            steps{

                git 'https://github.com/devopsstephen/June_carona.git'
            }
        }
        stage('package'){

           steps{
               sh 'mvn clean package'
           }
        }

        stage('deploy'){
            steps{
                sh '/opt/deploy.sh'
            }
        }


    }
}

