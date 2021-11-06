pipeline {



  agent any



  stages {



    stage('Checkout Source') {

      steps {

        git 'https://github.com/SriniGitAcc/wordpress-repo.git'

      }

    }





    stage('Deploy App') {

      steps {

        script {

          kubernetesDeploy(configs: "wordpress.yml", kubeconfigId: "mykubeconfig")

        }

      }

    }



  }



}
